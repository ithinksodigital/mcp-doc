

# Validate Your Identity System Configuration

Confirm and debug your identity system configuration.

### Required User Permissions

Permissions Needed  
---  
To configure the identity system: | A role with Administrator permissions  
  
  1. To confirm that the correct namespace is set, from the main navigation, select **Settings** | **Identity Types**. The **Identity Namespace** field at the top right of the page shows your dataset ID. 
  2. If the **Identity Namespace** field is blank, contact Salesforce Customer support to help you add it. 
  3. To verify that attributes match the correct Identity Types, select **Settings** | **Attributes**. 
  4. In the Attributes table, review each attribute’s Identity Type setting.
  5. To confirm events, select **Reports** | **Event Stream**. 
  6. In the Event Stream Report, make sure that events are sent in the proper format and that identity values are passed to the correct attributes. For more information, see the Developer Documentation [User Identity Mapping](https://developer.salesforce.com/docs/marketing/personalization/guide/user-identity-mapping.html?q=identity) and [Serverside Event API Requests](https://developer.salesforce.com/docs/marketing/personalization/guide/event-api-requests.html). 
  7. Verify that ETL formatting is correct. For more information, see [User ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5 "Use the User ETL data feed to update Unified Custom Profiles, and Unified Account Profiles if you have B2B Detect. Personalization stores user profiles for each anonymous and known user in the system.").
    1. Confirm that your ETLs are sent in the correct format to the correct attribute and that ETL formatting overall is correct. 
    2. Make sure that column headers are formatted correctly for your identity attributes and they’re in line with the expected column of data.
  8. If configured for your system, confirm that the Channel Identity Type is being used correctly. To check the identity type for each channel, see these setup help topics for the channels used in your system: [Mobile](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_mobile_apps.htm&language=en_US&type=5 "Use the Personalization identity system to identify and merge user profiles in your mobile app."), [Serverside](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_event_api.htm&language=en_US&type=5 "With Personalization’s identity system, you can configure the identifiers in the Event API to create Unified Customer Profiles for each of your customers. To merge user profiles from various sources, you designate an identity type to use when matching users between the Event API and Personalization. You can use multiple identifiers in the Event API."), [Web](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk.htm&language=en_US&type=5 "To create unified customer profiles for each of your customers, use Personalization’s identity system to configure the identifiers in the Marketing Cloud Personalization module of the Salesforce Interactions SDK. To merge user profiles from various sources, you designate an identity type to use when matching users between channels. You can use multiple identifiers in a web event."), [Email](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_open_time_email.htm&language=en_US&type=5 "To create unified customer profiles for each of your customers, use Personalization’s identity system to configure the identifiers in your Open Time Email campaigns. To merge user profiles from various sources, you designate an identity type to use when matching users between your email service provider and Personalization. You can use only one identity type. If you send multiple identifiers in an Open Time Email campaign, Personalization ignores all but the designated identity type.").

![49d255eb-1efd-4e67-9174-6015cddeda86]

Note Channel Identity Type is a dedicated identity type set for each channel.
This identity type identifies a known user for the specified channel. By
default, the identity type for each channel is set to the built-in
`customerId` identity. Changing the channel identity type after collecting
data with a previous identity can corrupt data and affect user merging.

  9. If your implementation uses Channel Identity Type, make sure that your sitemap and event sources from other channels use the identity type correctly. 

Send the value for the Channel Identity Type in events as `user.id`. For
example, if the Channel Identity Type for a web integration is configured to
be `customerId`, the sitemap for this integration must map the value for
`customerId` to `user.id`.

