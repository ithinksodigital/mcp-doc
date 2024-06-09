

# About Identity Types and Attributes

Learn about identity types and attributes.

## Setting Up the Identity System

![53b58805-a6f3-4ef0-8d9d-01fb8ca12a2c]

Note You must be a Personalization administrator to set up the identity
system. Salesforce employees who have been granted access to an account can’t
configure identities.

You set up the identity system during implementation before collecting data
through site mapping, data-driven events, or data feeds. The identity types
you select define a unique user profile within Personalization. After creating
an identity type, you associate it with user profile attributes to capture
specific user data.

Setting up the identity system is a permanent configuration. After you set up
an identity type, you can’t change it or delete it. Consider the implications
of identity management before configuring the identity system. Only configure
identity types and attributes that you require. Choose identity types based on
confidence, availability, and uniqueness. For example, if you set up First
Name as an identifier, Personalization merges every user named Bob to a single
user profile, and you can’t unmerge those users. There’s no way to split a
merged user profile.

If you're already collecting data and want to set up the identity system,
consider the following before proceeding:

  * When you set up the identity system, it only collects data from that point forward.

  * Any data that Personalization collected previously as a regular attribute doesn’t migrate to the identity system. For example, if you collect Customer ID as an attribute and then collect Customer ID as an identity type, the previously captured attribute data doesn’t migrate to the identity type.

  * Never set up an attribute that’s already collecting data as an identity type.

## Identity Type Uniqueness

An identity type’s uniqueness value determines whether the identity system can
use it for identity lookup and user profile merging. When you set up an
identity type, you select its uniqueness value.

When selecting a uniqueness value, keep these considerations in mind:

  * When merging user profiles, the identity system only considers identity types using the **Identity Namespace** uniqueness value.
  * ETL jobs can’t update an identity with a value of **Not Unique**.

Value | Description  
---|---  
Identity Namespace | The value can belong to only one user profile in the dataset, so Personalization can use it for identity lookup and user profile merging. For example, when using Email Address as the identity type, all user profiles with a unique email address belong to the same individual, so Personalization can merge them.  
Not Unique | The value can belong to multiple user profiles in the dataset, so Personalization can’t use it for identity lookup or user profile merging. For example, multiple users can have the same home phone number or mailing address, so Personalization can’t use those identity types for identity lookup and user profile merging. Personalization can use this value for searching.

