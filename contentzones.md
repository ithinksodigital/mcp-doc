# Server-Side Campaigns and Content Zones

The key difference between server-side campaigns and web campaigns is that
server-side campaigns do not require Content Zones. As a result, the server-
side template configurator does not have the Content Zone selector pane.

The following sections describe the differences in how Content Zones are used
for web and server-side campaigns.

Web campaigns require the Content Zone selector since Marketing Cloud
Personalization is responsible for rendering the campaign.

  * A template developer can assign one or more Content Zones to templates to determine where a particular template can be used on the site by a business user.
  * A business user targets a campaign to a specific Content Zone on the site and can then apply published templates that were tagged with that Content Zone by their template developer.

By linking web templates to specific Content Zones, a template developer
ensures that Personalization renders the experience correctly, as the template
was designed to work on that particular part of the site.

In a server-side campaign execution, the client takes responsibility for
rendering the response payload returned by Personalization. Since the output
of a server-side campaign is simply a data payload, template creation or
campaign targeting do not require Content Zone selection. In a server-side
campaign execution, it is up to the client to:

  * determine what data must be passed back as part of the campaign response (defined in server-side template)
  * apply the template to a campaign with appropriate targeting logic (Server-Side Campaign)
  * call Personalization's Event API and take the data it returns in the campaign response object and render it in the correct location/format

Clients that have implemented the Personalization Web SDK (with content zones
defined in the sitemap) and are using server-side campaigns to power
personalized experiences can leverage Content Zones to tie a server-side
campaign to a specific location on the site. Much like how a web campaign is
returned if the Content Zone is present on the page, a server-side campaign
that uses Content Zone targeting is also returned only if the targeted Content
Zone is present in the request. Adding a Content Zone to your server-side
template only requires a basic adjustment to the server-side code (the Content
Zone selector pane used for web campaigns is not available for Server-Side
campaigns).

In the server-side code, add the line `contentZone: "contentZone1" | "contentZone2"...`. Adding one or more Content Zone options will create the Content Zone dropdown selector in the business user template configurator. The template developer decides the number of Content Zones for which a template is eligible.

After you add a Content Zone to a server-side template, you must ensure that
you configure your API calling patterns correctly. Specifically, you need to
have `contentZones` included on the source object in the Event API request. A
template with a `contentZone` applied will only be returned in the response if
its targeted `contentZone` is present in the Event API request.

Personalization returns only one campaign response per `contentZone`.
Therefore, if you have two campaigns targeting the same `contentZone` and the
user is eligible for both, only one campaign is returned. A business user can
easily prioritize which campaign returns by assigning a priority value to the
campaign in the campaign configuration screen. As noted by the info icon next
to the priority input box (found in the **Campaign Type** window of the
campaign creation screen), campaigns with a higher numeric priority takes
precedence. If campaigns share a priority value, the campaign that was created
first wins.

The ONLY time a Content Zone requires a value in the server-side code as part
of a server-side campaign is for promotion selection/decisioning purposes.
Einstein Decisions requires that a Content Zone or tag is defined to filter
which promotion assets are eligible to be returned as part of the campaign
response. The Content Zone or tag you want to use as part of the Einstein
Decisions template would need to be hardcoded into the server-side template
code.

When previewing a server-side template in the in-app template editor, the
`contentZone` field in the **Payload Preview** shows a `NULL` value even if
you have a `contentZone` applied in the code or selected in the template
configuration. However, the selected/applied Content Zone works as desired
when the template is applied to a campaign, as that `NULL` value in the
simulator does not indicate that anything is wrong with the template.

The following code sample is an example of a server-side template with Content
Zones configured.

The following is an example Event API request for a server-side campaign that
leverages Content Zones.

