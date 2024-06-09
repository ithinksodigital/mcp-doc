# Event API Responses

Requests sent to the Event API return JSON that contains information about any
campaigns that are returned. A response from the Event API has the following
structure.

Key| Value| Description  
---|---|---  
`campaignResponses`| `CampaignResponse[]`| An array of all campaigns returned
in the event. For more information, see The CampaignResponse Object.  
`compiledCampaignTemplates`| `CompiledCampaignTemplate[]`| An array of all
campaign templates returned in the event. For more information, see The
CompiledCampaignTemplates Object.  
`errorCode`| Number| The error code. Possible values are:

  * 0 : Success 
  * 1 : Missing Encrypted `UserId` Parameter 
  * 2 : Invalid Encrypted `UserId` Parameter
  * 3 : Busy
  * 4: Anonymous ID Correction
  * 5: Invalid Event

  
`resolvedUserId`| String| The `primaryId` of the resolved User. The
`primaryId` is only returned if the **Pipeline Identity Resolution** feature
is enabled for the tenant. For more information, see [User Identity
Mapping](/docs/marketing/personalization/guide/user-identity-mapping.html).  
`persistedUserId`| Object| An object containing the encrypted user ID of the
user. The Event API returns the `persistedUserId` only if **Pipeline Identity
Resolution** isn’t enabled for the tenant and a primary user ID is specified
in the event. For more information, see [User Identity
Mapping](/docs/marketing/personalization/guide/user-identity-mapping.html).  
`eventDetails`| `eventDetails`| An object containing the event received by the
server. This object is only returned if `debug.explanations` was sent with the
event and the event was authenticated.  
  
The `CampaignResponse` object contains data associated with the campaigns
returned from an event.

Key| Value| Description  
---|---|---  
`type`| String| The type of campaign returned. The value of `type` is `"c"`
for server-side campaigns and `"ng"` for web campaigns.  
`campaignId`| String| The ID of the campaign returned.  
`campaignName`| String| The name of the campaign returned.  
`campaignType`| String| The type of the campaign returned. The value of
`campaignType` is `"ServerSide"` for server-side campaigns and `"Web"` for web
campaigns.  
`experienceId`| String| The ID of the experience returned.  
`experienceName`| String| The name of the experience returned.  
`state`| String| The state of the campaign returned. The value of `state` can
be `"Published"`, `"Disabled"`, or `"Testing"` depending on the campaign
state.  
`displayMode`| String| **Deprecated**. This object is only returned for
server-side campaigns and its value is always `"Personalized"`.  
`redirectUrl`| Null| **Deprecated**. This object is only returned for server-
side campaigns.  
`saveParameters`| Boolean| **Deprecated**. This object is only returned for
server-side campaigns and is always set to `false`.  
`hidePageBeforeRedirect`| Boolean| **Deprecated**. This object is only
returned for server-side campaigns and is always set to `false`.  
`campaignJavascriptContent`| Null| **Deprecated**. The
`campaignJavascriptContent` object is always set to `null`.  
`javascriptContent`| Null| **Deprecated**. This object is only returned for
server-side campaigns and is always set to `null`.  
`userGroup`| String| The user group of the campaign experience returned. The
value of `userGroup` can be either `"Default"` or `"Control"`.  
`googleAnalyticsConfig`| Null| **Deprecated**. This object is only returned
for server-side campaigns and is always set to `null`.  
`messages`| Empty array| **Deprecated**. This object is only returned for
server-side campaigns and is always set to `[]`.  
`pageChanges`| Empty array| **Deprecated**. This object is only returned for
server-side campaigns and is always set to `[]`.  
`templateNames`| String array| An array of the template names used in the
experience. This object is only returned for web campaigns.  
`serverSideMessages`| `ServerSideMessage[]`| An array of messages returned for
a server-side campaign. This object is only returned for server-side
campaigns. The event **must** be sent with `source.channel` set to `"Server"`
in order to return `serverSideMessages`. For more information, see
ServerSideMessage object.  
`payload`| `payload`| The payload object that the campaign returns. The
`payload` object always includes the `campaign`, `experience`, and `userGroup`
fields, along with other user defined fields. For more information, see
[Template Server Typescript](/docs/marketing/personalization/guide/template-
server-typescript.html). **Note:** The value of
`campaignResponse.payload.userGroup` can either be `"Test"` or `"Control"`.  
  
The `ServerSideMessage` object contains data associated with
`serverSideMessages` returned in a `campaignResponse`.

For server-side campaigns, an array of `ServerSideMessage` objects is returned
that contains information about the data returned for the server-side campaign
message. The event **must** be sent with `source.channel` set to `"Server"` in
order to return `serverSideMessages`. For more information on configuring
server-side campaigns, see [Server-Side
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign.htm).

Key| Value| Description  
---|---|---  
`type`| String| The type of message that is returned. For a
`ServerSideMessage`, the `type` is always `"evg_md"`.  
`id`| String| The ID of the message that is returned.  
`data`| String| **Deprecated**. Its value is always `"{}"`.  
`targetName`| String| The name of the target for the `ServerSideMessage`.  
`containsDynamicContent`| Boolean| The value returned is `true` if the message
contains any dynamic content, and `false` if the message doesn’t contain
dynamic content.  
`promotedItemKeys`| `PromotedItem[] | null`| If the message contains promoted items, `promotedItemKeys` is an array of promoted items. Otherwise its value is `null`. Each `PromotedItem` returned contains the type of the item returned and the `_id` of the item returned.  
`campaignState`| `"Published"`, `"Disabled"`, or `"Testing"`| The state of the
campaign returned.  
`dataMap`| `dataMap`| An object containing the key value pairs defined in the
campaign.  
  
The following is an example of a value returned in the `promotedItemKeys`
object:

The following is an example of a value returned in the `dataMap` object:

For keys with type "Promoted Content", the full value of each item is returned
unless the "Item IDs only" option is enabled in the message settings. For more
information on configuring server-side campaigns and the returned `dataMap`
object, see [Server-Side
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign_create.htm).

The `CompiledCampaignTemplates` object contains data associated with
`campaignTemplates` returned in an event.

An event response returns an array of any `compiledCampaignTemplates` used in
a `campaignResponse`. The `compiledCampaignTemplates` object contains
information about the campaign templates.

Key| Value| Description  
---|---|---  
`id`| String| The ID of the template.  
`name`| String or `null`| The name of the template.  
`bundle`| String| The stringified [client-side
code](/docs/marketing/personalization/guide/web-campaigns-templates.html) used
to render the template.  
  
The `CampaignExplanations` Object contains data associated with
`campaignExplanations` returned in an event.

The `campaignExplanations` object returns in an event only if
`debug.explanations` is `true` in the event payload. It contains additional
information about why campaigns did or didn’t return in the event response.
It’s only returned if the event request is authenticated.

Key| Value| Description  
---|---|---  
`class`| String| Information of the type of explanation that is returned.  
`campaignId`| String| The ID of the campaign that the explanation is for.  
`campaignName`| String| The name of the campaign that the explanation is for.  
`experienceId`| String| The ID of the experience that the explanation is for.  
`experienceName`| String| The name of the experience that the explanation is
for.  
`messageId`| String| The ID of the message that the explanation is for.  
`explanationMessage`| String| A message containing the reason for not
returning the campaign in the response.  
`context`| String| A string containing the campaign name, campaign ID,
experience name, and experience ID for the message that isn't returned in the
response.  
  
  * [_Salesforce Help_ : Server-Side Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign.htm)

