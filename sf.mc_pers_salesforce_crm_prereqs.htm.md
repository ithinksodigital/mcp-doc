

# Prerequisites and Considerations for Salesforce CRM Integration

Before integrating Marketing Cloud Personalization with Salesforce CRM, review
these requirements and considerations.

## Prerequisites

  * You must have an Enterprise or higher Salesforce CRM account. 
  * Advanced expertise and permissions are required. You must have ModifyAllData permissions, as well as an intermediate or advanced level of expertise in Salesforce CRM.
  * You need a field that you can use to map users and accounts between Personalization and Salesforce CRM. Typically, this field is an email address. You must capture this field in both Personalization and Salesforce CRM.

## Minimum Security Requirements for Integration

For | Description  
---|---  
User | The profile of the user establishing the OAuth connection must have the `ModifyAllData` permission. Personalization needs this permission to create custom fields using the Metadata API.   
OAuth | The Connected App that Personalization uses must include the following OAuth scopes: 

  * Access your basic information (ID, profile, email, address, phone)
  * Access and manage your data (API)
  * Perform requests on your behalf at any time (refresh_token, offline_access)

  
Field | Each Salesforce contact, account, or lead field created by Personalization must be made visible to the profile of the Salesforce user used to establish the OAuth connection. You can manually making each field visible after it has been created by Personalization.   
  
For additional information, see [Viewing a Profile's Assigned
Users](https://help.salesforce.com/s/articleView?id=sf.users_profiles_assigned_users.htm&language=en_US&type=5)
and [ Field Level
Security](https://help.salesforce.com/s/articleView?id=sf.admin_fls.htm&language=en_US&type=5).

## Integration Considerations

  * This integration doesn’t create user records in either Salesforce CRM or Personalization. It shares user attribute data only for existing, known users in both platforms.If you want to import users from external systems into Personalization, see [User ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5 "Use the User ETL data feed to update Unified Custom Profiles, and Unified Account Profiles if you have B2B Detect. Personalization stores user profiles for each anonymous and known user in the system.").
  * There’s no data sharing between this integration and the Personalization user identity system. This integration is a mechanism for matching and updating attributes. It doesn’t create contacts, populate identities, or merge identities.

#### See Also

  * [About Integrating Personalization with Salesforce CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_about.htm&language=en_US&type=5 "Learn about sharing data between Marketing Cloud personalization and Salesforce CRM.")

