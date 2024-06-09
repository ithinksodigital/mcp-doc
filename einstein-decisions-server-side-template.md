# Einstein Decisions - Server-Side Template

When using Einstein Decisions in a template, a slightly different server-side
code configuration is necessary for a server-side template than a Web
template. This article describes the fundamental differences between the two
types of templates concerning the following two critical parts of the
template.

  * What content zone or tag the bandit leverages for decision-making
  * What data is returned on the promotion

The Global Web Template leverages `context.contentZone` to determine which
promotion content zone is to be evaluated for a decision by Einstein
Decisions. The `context.contentZone` value maps to the targeted web content
zone of the template, meaning the targeted web content zone serves the
following two purposes.

  * Determining where the Einstein Decisions template is allowed to render on the site
  * Filtering which promotions are eligible to be returned by the template (only promotions with an asset that has a content zone or tag that maps to the targeted web content zone are eligible for decision-making)

To configure the targeted web content zone, you can use the **Content Zones in
Template** selector in the Web Template Editor to select a single value or
define a set of values for business users to pick from via a dropdown menu.

![d10e2998-83a4-435b-b870-8dd3f07e11da]

By leveraging `context.contentZone` in the template, you effectively restrict
which promotions can be returned. Since the **Content Zones in Template**
selector in the Web Template Editor only displays web content zones defined in
the sitemap, only promotions with an asset tied to a web content zone are
eligible to return.

The Global Web Template returns the primary data required for client-side
rendering. In this case, the template is set to return just the image URL for
the selected asset and the promotion URL. You can easily configure additional
promotion attributes/information to return via the web template.

The server-side iteration of the template gives you a little more flexibility.
Since the **Content Zones in Template** selector leveraged in web templates is
not available in the server-side template interface, use `ContentZoneLookup`
instead of referencing `context.contentZone`. Unlike the web content zone
selector, `ContentZoneLookup` is not restricted to only content zones defined
in the sitemap. Instead, it enables a business user to select any content zone
or tag value stored against a promotion asset or defined in the sitemap. The
value that a business user selects will reflect the promotion content zone or
tag that Einstein Decisions then leverages for real-time evaluation and
decision-making.

Since Marketing Cloud Personalization is not responsible for rendering the
decision passed back via a server-side campaign, the Server-Side template is
designed to return all promotion information for the selected promotion by
default. You can easily restrict what is returned in the response if the
complete promotion data is not required.

Additionally, since the complete promotion data is being returned, as opposed
to asset-specific data like an image URL, a business user only needs to define
a fallback promotion as opposed to a fallback promotion along with a fallback
asset.

To properly train the contextual bandit, it is essential to ensure click log
generation. The Einstein Decisions global web template automatically tracks
click logs and view logs in web campaigns. However, only view logs are tracked
automatically in server-side Einstein Decisions campaigns, while clicks
require manual tracking.

This section outlines two approaches for ensuring the proper capture of click
logs.

This option requires `contentZone` to be set on the experience. You can set
`contentZone` on the experience in server-side campaigns by returning the
`contentZone` explicitly through the server-side template's `run` function.

The following code depicts an example template for this approach.

In the preceding template configuration, note that the selected `contentZone`
in the template configuration screen gets applied to the experience.
Therefore, for this campaign/experience to return, the inbound event request
to Personalization must include a matching `contentZone` value on the `source`
object. The campaign does not return if there is no matching `contentZone`
value on the inbound event.

If the desired `contentZone` is unknown when sending an event request to
Personalization, we recommend leveraging Option 2, which allows you to avoid
setting a `contentZone` on the campaign/experience to ensure that the campaign
can return without a `contentZone` being specified on the `source` object on
the inbound event.

The following code depicts the formatting of an example `stat` event using the
preceding template.

As mentioned in Option 1, using the template configuration that sets the
`contentZone` via the `run` function means that the experience only returns
when `contentZone` is present in the original event. If the `contentZone` is
unknown at the campaign request time, you can use the following template
configuration and ensure click log generation using a modified `stat` event
that includes the `contentZone` leveraged in the campaign decision. The only
difference between the following template and the preceding one is the
`return` object of the `run` function.

The following code depicts the formatting of an example `stat` event to ensure
proper click log generation using the preceding template.

The preceding `stat` event includes the standard click campaign `stat` object
that populates the clicks against the campaign and the promotion on the
promoted item detail stat screen. This `stat` event is different from the
`stat` event outlined in Option 1 in the following key ways.

  * **`contentZone` included on the `source` object**: In Option 1, the `contentZone` is set on the campaign/experience and is therefore not required in the `stat` event. In this option, since the `contentZone` is not set on the campaign/experience, it needs to be included on the `stat` event to allow for click log generation to support model training. The `contentZone` or tag selected in the template configuration for decisioning purposes is available on the campaign response object as the `assetContentZoneOrTag` value. The web developer configuring the `stat` event can easily reference that value to populate the `contentZone` value on the `stat` event.

  * **`Click Through` Item Action**: This item action is only leveraged in this specific instance to track clicks on the promotion object. Paired with the `contentZone` on the `source` object, this item action causes click logs to be generated for model training.

When sent to Personalization, a single event has to include the campaign stat
object and the `Click Through` item action object.

The `return` object in the first template sets the selected asset content zone
or tag as the `contentZone` on the experience and campaign response object,
while this template does not. Instead, it leaves the `contentZone` value
blank.

