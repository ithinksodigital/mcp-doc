

# About Integrating Personalization with Salesforce CRM

Learn about sharing data between Marketing Cloud personalization and
Salesforce CRM.

## Send Data from Personalization to Salesforce CRM

Share with Salesforce CRM the deep behavioral insights about visitors and
customers that interact with your website, web application, and mobile app.

## Send Data from Salesforce CRM to Personalization

Share with Personalization any text field, dropdown menu, numeric value, or
segment data so you can use it to deliver personalized experiences in real
time.

## Bulk API Calls During Data Sharing

Personalization uses API calls to create a Data Loader job for contacts,
leads, and accounts as configured.

  * Every 1,000 Personalization users or accounts that could match Salesforce CRM contacts, leads, and accounts are validated in an API call.
  * Up to 10,000 matches are pushed in a batch through an API call.
  * Job progress is intermittently checked through API calls.
  * Job results are validated for each batch through API calls.

For more information, see [Enable Bulk
API](https://developer.salesforce.com/docs/atlas.en-
us.250.0.dataLoader.meta/dataLoader/loader_configuring_bulk_api.htm).

## Summary of Integration Tasks

# | Task  
---|---  
1 | [Prerequisites and Considerations for Salesforce CRM Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_prereqs.htm&language=en_US&type=5 "Before integrating Marketing Cloud Personalization with Salesforce CRM, review these requirements and considerations.")  
2 | [Plan Data Sharing Between Personalization and Salesforce CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization.htm&language=en_US&type=5 "Before initializing data sharing, decide what data you want to exchange between Salesforce CRM and Personalization and how you want to match data for merging. After initialization, Marketing Cloud Personalization shares data with Salesforce CRM on a nightly basis. Contacts and accounts are shared automatically, but leads sharing is optional.")  
3 | [Set Up Integration with Salesforce CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_integrate.htm&language=en_US&type=5 "Complete these steps to set up the integration between Marketing Cloud Personalization and Salesforce CRM.")  
4 | [Set Up Automated Data Sharing Between Personalization and Salesforce CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization_initialize.htm&language=en_US&type=5 "After you configure automated data sharing, Marketing Cloud Personalization and Salesforce CRM share data on a nightly basis.")  
5 | [Show Personalization Data in Salesforce CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_view.htm&language=en_US&type=5 "In Salesforce CRM, display data that was shared by Marketing Cloud Personalization. For shared contacts, accounts, and leads, configure the applicable record layout in Salesforce CRM.")

