

# Identity System for Mobile Apps

The Personalization identity system enables you to select a default identity
attribute to match users between your mobile application and Personalization.
Personalization uses only one identity attribute in looking up and merging
mobile app events.

Before configuring an identity attribute for your mobile app, make sure to
review this information.

  * [Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5 "Personalization’s identity system uses deterministic matching to create a Unified Customer Profile for each of your customers. Specific identifiers, called identity types, determine how to process web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. If the built-in identity types don’t meet the needs of your organization, you can create additional identity types.")
  * [Built-In Identity Types](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_built_in.htm&language=en_US&type=5 "Identity types are specific identifiers that determine how Personalization processes web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. The built-in identity types don’t require configuration other than setting up event capture mechanisms, such as the sitemap or ETL jobs.")

By default, Personalization uses the built-in customer ID identity type as the
identifier for mobile apps. However, you can change the identity type that
Personalization uses for identity lookup and merging user profiles. For
example, if you have a loyalty ID as an identity type, you can use that value
for lookup and merge.

When selecting an identity attribute, keep these considerations in mind.

  * You must choose one default identity attribute for lookup. You can’t select multiple attributes for lookup, such as both email address and customer ID.
  * Personalization uses only the configured default identity for lookup and merge. If you send multiple identities in a mobile event, Personalization uses only the configured default identity for lookup and merge. All other identities in the event are ignored and not processed.

#### See Also

  * [Configure the Identity System for Mobile Apps](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_mobile_apps_configure.htm&language=en_US&type=5 "Select the identity attribute that Personalization uses for identity lookup and merging user profiles in mobile apps. If you have active mobile app campaigns, changing this setting can impact the content that appears for those campaigns.")
  * [ _Developer Documentation_ : Marketing Cloud Personalization Mobile Integration](https://developer.salesforce.com/docs/marketing/personalization/guide/mobile-integration.html)

