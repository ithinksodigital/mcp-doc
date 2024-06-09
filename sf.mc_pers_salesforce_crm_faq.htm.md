

# FAQs for Personalization Integration with Salesforce CRM

Answers to common questions about the integration between Marketing Cloud
Personalization and Salesforce CRM.

## How many API calls does Marketing Cloud Personalization use to share data
with Salesforce CRM?

Personalization shares data using the Data Loader and bulk API calls. For more
information, see “Bulk API Calls During Data Sharing” in [About Integrating
Personalization with Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_about.htm&language=en_US&type=5
"Learn about sharing data between Marketing Cloud personalization and
Salesforce CRM.").

## What can I do if the account names for a contact differ in Personalization
and Salesforce CRM?

Often, the account name in Personalization does not exactly match the account
name in Salesforce CRM. To remedy account merge issues, see “Match and Merge
Lead Data” in [Plan Data Sharing Between Personalization and Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization.htm&language=en_US&type=5
"Before initializing data sharing, decide what data you want to exchange
between Salesforce CRM and Personalization and how you want to match data for
merging. After initialization, Marketing Cloud Personalization shares data
with Salesforce CRM on a nightly basis. Contacts and accounts are shared
automatically, but leads sharing is optional.").

## What should I do if I make a change to OAuth security settings in
Salesforce CRM?

Changes to any Salesforce security settings–at the OAuth App, the Salesforce
User, or the Field security level–can disrupt the integration. If the
integration is not working as expected after changing security settings, then
you must reconfigure the integration and test your changes.

## What are the minimum security requirements for the integration?

The integration has minimum security requirements for Salesforce users, OAuth,
and fields. For more information, see “Minimum Security Requirements for
Integration” in [Prerequisites and Considerations for Salesforce CRM
Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_prereqs.htm&language=en_US&type=5
"Before integrating Marketing Cloud Personalization with Salesforce CRM,
review these requirements and considerations.").

## How does Personalization match contacts, accounts, and leads?

Personalization matches contacts, accounts, and leads according to the
criteria described in [Plan Data Sharing Between Personalization and
Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization.htm&language=en_US&type=5
"Before initializing data sharing, decide what data you want to exchange
between Salesforce CRM and Personalization and how you want to match data for
merging. After initialization, Marketing Cloud Personalization shares data
with Salesforce CRM on a nightly basis. Contacts and accounts are shared
automatically, but leads sharing is optional.").

#### See Also

  * [About Integrating Personalization with Salesforce CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_about.htm&language=en_US&type=5 "Learn about sharing data between Marketing Cloud personalization and Salesforce CRM.")

