# Tracking Personalization Web Campaign Statistics

The Campaign Stats Gear tracks impressions, clickthroughs, dismissals, and
recommended items on your Marketing Cloud Personalization campaigns. These
statistics give you insight into the effectiveness of these campaigns and help
you decide where to adjust your campaigns for better results.

Most organizations use third-party analytics software to track campaign
effectiveness, in addition to using Personalization Campaign Statistics. In
such cases, it is possible that Personalization campaign statistics differ
from statistics gathered via third-party software. This difference is mainly
because tracking parameters and their definitions on Personalization can vary
from how they're defined, handled, and tracked in third-party systems.

A campaign's DOM structure must meet specific requirements to correctly track
statistics in Personalization.

Campaign statistics are necessary for analytics in Personalization, analytics
events emitted to external systems, segment creation, campaign targeting, and
machine learning optimization.

Use the following HTML data attributes in order to properly track campaign
statistics using the Campaign Statistics gear.

Attribute| Description| Use in Template Handlebars  
---|---|---  
`data-evg-campaign-id`| The ID of the campaign. This attribute must be
specified for any client-rendered web campaigns.| `data-evg-campaign-
id="{{campaign}}"`  
`data-evg-experience-id`| The ID of the experience. This attribute must be
specified for any client-rendered web campaigns. By default, clicks on any
`<a>` tags nested within an element containing this attribute are tracked.|
`data-evg-experience-id="{{experience}}"`  
`data-evg-user-group`| The group that the user belongs to. This group is
either the test or control group.| `data-evg-user-group="{{userGroup}}"`  
`data-evg-clickthrough`| Indicates that this element is clickable. This
attribute can be added to any element with no value to indicate that it should
generate a clickthrough when clicked. Note that it is unnecessary to add this
value to `<a>` tags that are children of an element with the `data-evg-
experience-id` element.| `data-evg-clickthrough`  
`data-evg-ignore-clickthrough`| Indicates that this element is clickable, but
should not have a clickthrough tracked for it. This attribute can be added
with no value to any element or ancestor of the clickable element.| `data-evg-
ignore-clickthrough`  
`data-evg-dismissal`| Indicates that this element is dismissible. This
attribute can be added to any element with no value to indicate that it should
generate a dismissal when clicked.| `data-evg-dismissal`  
`data-evg-item-id`| The ID of the item represented by this element and its
child elements. This ID (and the type specified by `data-evg-item-type`) must
already be tracked in the Personalization catalog. Adding this attribute to an
element, along with `data-evg-item-type`, binds and tracks clickthroughs.|
`data-evg-item-id="{{id}}"`  
`data-evg-item-type`| The type of the item represented by this element and its
child elements. This type (and the ID specified by `data-evg-item-id`), must
already be tracked in the Personalization catalog. Adding this attribute to an
element, along with `data-evg-item-id`, binds and tracks clickthroughs.|
`data-evg-item-type="{{itemType}}"`  
  
  * To track promotions accurately using this gear, your campaign template must include the `data-evg-item-id` and `data-evg-item-type` attributes. The updated Einstein Decisions template includes these attributes by default. Cloning this template and applying it to your campaign enables promotion tracking by default.
  * Personalization will display campaign statistics for unpublished campaigns that you're testing. Although unpublished, the Campaign Stats Gear can still track and increment campaign statistics on these campaigns.

When a campaign is returned to the web browser, the user is in either a "Test"
group or the "Control" group. If the user is in a "Test" group, a template's
client-side code executes the `apply()` function. Likewise, if the user is in
the "Control" group, a template's client-side code executes the `control()`
function. Both functions can return either a `Promise` or `void`. For more
information, see the [Template Client
JavaScript](/docs/marketing/personalization/guide/template-client-
javascript.html) documentation.

If the `apply()` function doesn't return a `Promise`, Personalization
dispatches the `Evergage.CustomEvents.OnTemplateDisplayEnd` event immediately,
subsequently triggering the Campaign Stats Gear to begin tracking campaign
statistics even before the template may have fully rendered.

For more information on the `apply()` function, refer to the [Template Client
JavaScript](/docs/marketing/personalization/guide/template-client-
javascript.html#apply) documentation.

The "Control" experience _does not_ necessarily need to render HTML into the
DOM for Campaign Stats Gear to track a "Control" impression. For instance, an
impression stat is tracked immediately if the `control()` function does not
return a `Promise`.

The following code samples are examples of how you can return a Promise in an
`apply()` function using [the `pageElementLoaded` method from
`DisplayUtils`](/docs/marketing/personalization/guide/web-template-display-
utilities.html) in the `SalesforceInteractions` and `Evergage` namespaces.

The following code samples are examples of how you can return a Promise in an
`apply()` function using a `new Promise`.

If your site does not use Handlebars and Client-side Code in a Personalization
template to render campaigns, you can still use the Campaign Stats Gear to
track campaign statistics.

When you are ready to track an impression for a Personalization campaign,
dispatch an `SalesforceInteractions.mcis.CustomEvents.OnTemplateDisplayEnd`
event or `Evergage.CustomEvents.OnTemplateDisplayEnd` event, depending on the
SDK namespace you're using, with the following `detail`.

The following code samples depict how you can dispatch a
`SalesforceInteractions.mcis.CustomEvents.OnTemplateDisplayEnd` or
`Evergage.CustomEvents.OnTemplateDisplayEnd` event with an example payload.

In order to track clicks in the control group, the data attributes must be
added to elements that are either rendered by the campaign, or exist on site
and a user in the control group would see. See the following code samples for
guidance on adding these attributes in the `control()` function.

If you're using a DisplayUtil such as `pageElementLoaded` in the template's
`apply` function, then it is also _strongly suggested_ that you use it
similarly in the `control` function to ensure that campaign stats are being
tracked the same way.

`SalesforceInteractions.mcis.sendStat` and `Evergage.sendStat` accept a
`CampaignStatEvent`.

The following code samples depict how you can use
`SalesforceInteractions.mcis.sendStat` or `Evergage.sendStat` to send a
`CampaignStatEvent` event with recommended items.

