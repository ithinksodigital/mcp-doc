

# Create an Identity Type

Personalization includes several built-in identity types, such as email
address and customer ID. However, if the built-in identity types don’t meet
the needs of your organization, you can create three additional identity
types. After you create an identity type, you can’t edit it or delete it.

### Required User Permissions

Permissions Needed  
---  
To create an identity type: | A role with Administrator permissions  
  
Before creating an identity type, make sure to review this information.

  * [Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5 "Personalization’s identity system uses deterministic matching to create a Unified Customer Profile for each of your customers. Specific identifiers, called identity types, determine how to process web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. If the built-in identity types don’t meet the needs of your organization, you can create additional identity types.")
  * [Built-In Identity Types](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_built_in.htm&language=en_US&type=5 "Identity types are specific identifiers that determine how Personalization processes web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. The built-in identity types don’t require configuration other than setting up event capture mechanisms, such as the sitemap or ETL jobs.")

![e300e075-64bd-4b19-a8eb-bda554aff970]

Important Set up the identity system during implementation, before collecting
any data in your production dataset.

  1. From the main navigation, select **Settings** | **Identity Types**.
  2. Click **Add new record**.
  3. Enter an **ID**. The ID is a unique identifier for the identity type by entering alphanumeric characters without spaces, such as “SecondaryEmail.”
  4. Enter a descriptive **Label** for the identity type, for example, Secondary Email Address.
  5. Select a **Uniqueness** value for the identity type.

![42f8fa00-1177-4412-b334-0c745f33f737]

Note When merging user profiles, the identity system only considers identity
types with **Identity Namespace** uniqueness values.

Value | Description  
---|---  
Identity Namespace | The value can belong to only one user profile in the dataset, so Personalization can use it for identity lookup and user profile merging. For example, if you use Email Address as the identity type, all user profiles with a unique email address belong to the same individual, so Personalization can merge them.  
Not Unique | The value can belong to multiple user profiles, so Personalization can’t use it for identity lookup or user profile merging. For example, multiple users can have the same home phone number or mailing address, so Personalization can’t use those identity types for identity lookup and user profile merging. Personalization can use this value for searching.  
  
  6. Specify whether identifiers are **Case-Sensitive**. 

Select **True** for a case-sensitive identifier or **False** for a case-
insensitive identifier. For example, with a case-sensitive customer ID,
“ABC123” and “abc123” are two separate IDs because they don’t match.

  7. To save the identity type, click the check mark icon.
  8. From the main navigation, select **Settings** | **Attributes**.
  9. On the **User Attributes** tab, click **New Attribute**.
  10. Select the identity type you created from the **Identity Type** dropdown.
  11. Enter a **Name** for the identity attribute. Ideally, match the name to the identity type’s ID.
  12. Enter a **Label** that describes the attribute.

The label appears in the Unified Customer Profile.

  13. Select **String** as the attribute **Type**.
  14. Select an option from the **Classification Override** dropdown.

Option | Description  
---|---  
Sensitive | The attribute displays only to admins or people with a role that includes User/Account Profile > View Sensitive permissions, and you can’t use the attribute in a campaign. People with lesser permissions see asterisks instead of sensitive values in the Unified Customer Profile and segment lists. Additionally, email address fields (with a name of "emailAddress") aren’t searchable.  
Personally Identifiable | Anyone can view the attribute, but you can’t use the attribute in a campaign.  
Nonsensitive | Anyone can view the attribute, and you can use the attribute in a campaign.  
  
  15. To save the identity type, click the checkmark icon.
  16. Create additional user attributes as necessary, up to a maximum number of 100 user attributes per dataset.

