

# About Identity System Setup for Open Time Email

Learn about setting up the identity system for open time email campaigns.

## Before You Configure

Before configuring Personalization’s identity system for Open Time Email
campaigns, make sure to review this information:

  * [Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5 "Personalization’s identity system uses deterministic matching to create a Unified Customer Profile for each of your customers. Specific identifiers, called identity types, determine how to process web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. If the built-in identity types don’t meet the needs of your organization, you can create additional identity types.")
  * [Built-In Identity Types](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_built_in.htm&language=en_US&type=5 "Identity types are specific identifiers that determine how Personalization processes web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. The built-in identity types don’t require configuration other than setting up event capture mechanisms, such as the sitemap or ETL jobs.")

## Identity Types in Open Time Email Campaigns

The built-in email address identity type is the default identifier for Open
Time Email campaigns. You can change the identity type that Personalization
uses for identity lookup and merging user profiles. For example, if you have
email address and loyalty ID as identity types, you can use the loyalty ID
instead of email address.

![a320ac4e-605e-4959-97bd-6371d4bb2d50]

Note Open Time Email campaigns require an identity type value of at least four
characters.

