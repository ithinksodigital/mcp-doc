# Interaction Event Options in the SalesforceInteractions Namespace

The following code sample details the event options available in the
`SalesforceInteractions` namespace in the Personalization module of the
Salesforce Interactions SDK.

The `interaction` object has the following structure.

You can use the `Interaction` field to capture user engagement data. The
`Interaction` field has the following structure.

This type of `Interaction` is used to capture engagement data about catalog
objects.

You can use the `location` object to send location data on a `catalogObject`
via the Event API or using the Sitemap. The following is an example of how to
structure a `catalogObject` to include location data.

The following examples depict sending data for locations outside the US.

This type of `Interaction` is used to capture engagement data about the
contents of a user's cart.

This type of `Interaction` is used to capture engagement data about the items
in a user's order. Only the `PurchaseOrderInteraction` affects and updates a
user's current order.

A `LineItem` represents a single item in a cart and/or transaction. A
`LineItem` object has the following structure.

The following table describes the properties that a `LineItem` object accepts.

Property| Value Type| Description  
---|---|---  
`catalogObjectType`| String| The type representing the catalog object.  
`catalogObjectId`| String| A unique ID representing the catalog object.  
`quantity`| Number| The number of catalog objects in the line item.  
`price`| Number| The price of the catalog object in the line item.
**Important:** `price` is mandatory only when using `LineItem` in a purchase
or cart interaction, and optional for other interactions.  
`currency`| String| Optional. Currency code of purchase. If currency is
unspecified or `null`, it defaults to the dataset's configured currency.  
`attributes`| `{[key: string]: string | number | boolean }`| Optional. Key-value pairs that are stored as metadata on the `LineItem`. You can include `sku` within `attributes`.  
  
The following is an example of a line item used within an `AddToCart`
interaction.

The `consent` field accepts an array of consent objects for the user. The
following table describes the various properties available in the `consent`
object.

Property| Value Type| Description  
---|---|---  
`purpose`| String| The purpose for the consent. For example,
`Personalization`.  
`provider`| String| The consent provider  
`status`| String| The consent status. For example, `OptIn` or `OptOut`  
  
The `debug` object contains fields that help investigate issues that could
arise when developing campaigns.

The following table describes the properties available in the `debug` object.

Property| Value Type| Description  
---|---|---  
`testMessages`| String| A comma-separated list of campaign experience IDs to
be forced to return in the event, ignoring rules that would otherwise prevent
the campaign from returning. Alternatively, you can use the string value
`true` to return all campaigns in testing mode but all rules are respected.  
  
The `flags` object contains properties that alter default event processing. By
default, all flags are `false` if not present on the event.

The following table describes the various properties available in the `flags`
object.

Property| Value Type| Description  
---|---|---  
`noCampaigns`| Boolean| If `true`, don’t return campaigns in the response.  
`nonInteractive`| Boolean| If `true`, a visit isn’t created (or updated) for
the given user in the event. Additionally, no visit referrer nor originating
referrer is created for the user.  
  
The `Source` object contains properties that help describe where an event is
coming from. This object has the following structure.

The following table describes the various properties available in the `Source`
object.

Property| Value Type| Description  
---|---|---  
`channel`| String| The originating source of the event (For example, `Web`,
`MobileApp`, `CallCenter`).  
`application`| String| The originating application level source of the event
(For example, `ReactApp`, `3rdParty`, `ReactNative`)  
`pageType`| String| The type of page from which you’re sending the event (For
example, `PDP`, `Blog`, `Pricing`).  
`url`| String| The URL of the page from which you’re sending the event.  
`urlReferrer`| String| The previous URL visited by the user. `urlReferrer` is
populated from `document.referrer` by default on the web. It can be
overwritten in the sitemap to any other value if necessary.  
`locale`| String| The locale of the current page, as defined by ISO 639
alpha-2 language codes and ISO 3166 alpha-2 country codes (For example,
`en_US`, `de_DE`).  
`contentZones`| `string[]`| An array of content zones on the current page.  
`configVersion`| Number| Version number of the configuration for the SDK.  
`userAgent`| String| The user agent for the event. `userAgent` is populated
automatically but can be overwritten if necessary  
`clientIp`| String| The IP Address sending the event. `clientIp` is populated
automatically but can be overwritten if necessary  
`operatingSystem`| String| Only applicable for mobile events.  
`operatingSystemVersion`| String| Only applicable for mobile events.  
`device`| String| Only applicable for mobile events.  
`surveyId`| String| The ID of the survey being submitted. Set automatically
for events sent through the Survey Gear  
`surveyStartTime`| String| The start time of the survey being submitted. Set
automatically for events sent through the Survey Gear  
  
The `User` object describes the user associated with an event.

The following table describes the various properties available in the `user`
object.

Property| Value Type| Description  
---|---|---  
`anonymousId`| String| The ID of an anonymous user.  
`identities`| `[key: string]: string`| Key-value pairs that are stored as
identity information of a user.  
`encryptedId`| String| The encrypted ID returned from an event that contains
the ID field. Encrypted IDs are returned in the response to events that
provide identities.  
`attributes`| `{ [key: string]: string | number | boolean }`| Key-value pairs that are stored as metadata on the user. These attributes must be defined in the platform.  
`profileObjects`| `{ [profileObjectType: string]: ProfileObject[] }`| Key-
value pairs of profile objects that are stored as metadata on the user.
Profile objects, their attributes, and related catalog objects must be defined
in the platform.  
  
You can use the `profileObjects` field to send new or update existing profile
objects via the Event API or using the Web SDK. You can send multiple profile
objects of one type or multiple types in a single event.

To enable **Strict Profile Object Security** , log on to the Personalization
UI and navigate to **Settings** > **Catalog and Profile Objects** > **User
Profile Object Settings**. Enabling this setting restricts profile object
updates to authenticated event sources such as ETL and Event API calls that
use `channel: Server` and the `/authevent` endpoint. After it’s enabled,
updates to profile objects from unauthenticated channels such as `Web` are
ignored.

  * If an event causes a user to exceed 100 profile objects of a specific type, the 100 most recent objects are retained based on their creation date.
  * You can’t selectively update the fields of a profile object. You can only replace each instance of a profile object entirely. If you're updating an existing profile object, fields in the incoming event entirely replace the user's existing profile object fields.
  * A set of profile objects of a given type can’t be entirely replaced by another set or an empty set. For example, an event with `profileObjects: { Lease: [] }` doesn't clear out all `Leases` on that given user.
  * You can only create new or replace existing profile objects with Event API calls and not remove them.

The following table describes the properties that a `ProfileObject` accepts.

Property| Value Type| Description  
---|---|---  
`id`| String| The ID of a Profile Object.  
`relatedCatalogObjects`| `{ [catalogObjectType: string]: string[] }`| Related
catalog objects key-value pairs. These related catalog objects must be defined
in the platform.  
`attributes`| `{ [key: string]: string | number | boolean }`| Attribute key-value pairs that are stored as metadata on the profile object record. These attributes must be defined in the platform.  
  
The following example depicts sending a single “Lease” profile object record
with attributes and related catalog objects.

The `Account` object describes the account associated with an event.

The following table describes the various properties available in the
`account` object.

Property| Value Type| Description  
---|---|---  
`id`| String| The ID of an account.  
`attributes`| `{ [key: string]: string | number | boolean }`| Key-value pairs that are stored as metadata on the account. These attributes must be defined in the platform.  
  
The `PerformanceMetrics` object has properties that measure loading, parsing,
and network performance.

The following table describes the various properties available in the
`PerformanceMetrics` object.

Property| Value Type| Description  
---|---|---  
`sdkLoadTimeMs`| Number| (Web SDK) Time, in milliseconds, for the network to
load the web SDK.  
`sdkParseTimeMs`| Number| (Web SDK) Time, in milliseconds, for the beacon to
be parsed during page load.  
`pageLoadTimeMs`| Number| (Web SDK) Time, in milliseconds, for the DOM to
load.  
`networkTimeMs`| Number| (Web SDK) Time, in milliseconds, for the previous
request to return.  
  
You can use the `campaignStats` object to track campaign statistics for an
associated event.

For more information on sending campaign statistics on the web, refer to the
[Campaign Stats Tracking](/docs/marketing/personalization/guide/campaign-
stats-tracking.html) documentation.

The `campaignStats` object has the following structure.

The `CampaignStat` object has the following structure.

The following table describes the properties a `CampaignStat` object accepts.

Property| Value Type| Description  
---|---|---  
`experienceId`| String| The experience ID of the campaign on which the given
statistic is being tracked  
`stat`| `"Impression" | "Click" | "Dismissal"`| The type of statistic being tracked.  
`control`| Boolean| If `true`, the statistic is tracked for the control group
of the given experience.  
`catalog`| `{ <ItemType>: string[] }`| A mapping of catalog item types to a
list of corresponding item IDs on which to attribute the given statistic.  
  
The following is an example of a mapping of catalog item types.

