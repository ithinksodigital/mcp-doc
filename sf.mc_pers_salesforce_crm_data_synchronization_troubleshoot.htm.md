

# Troubleshoot Personalization Integration with Salesforce CRM

Troubleshoot common issues with the integration between Marketing Cloud
Personalization and Salesforce CRM. Changes to any Salesforce CRM security
settings—at the OAuth App level, the Salesforce User level, or the Field
Security level—can disrupt the integration.

### Required User Permissions

Permissions Needed  
---  
To troubleshoot data synchronization: | A role with Administrator permissions  
  
  1. If the integration isn’t working as expected, and you have made security changes, you must reconfigure the integration. 

Follow the steps in [Integrate Personalization with Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm.htm&language=en_US&type=5
"Share data between Marketing Cloud Personalization and Salesforce CRM. Send
Personalization user and visitor information to Salesforce CRM. Receive CRM
data associated with text fields, dropdown menus, numeric values, or
segments."), [Set Up Automated Data Sharing Between Personalization and
Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization_initialize.htm&language=en_US&type=5
"After you configure automated data sharing, Marketing Cloud Personalization
and Salesforce CRM share data on a nightly basis."), and [Show Personalization
Data in Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_view.htm&language=en_US&type=5
"In Salesforce CRM, display data that was shared by Marketing Cloud
Personalization. For shared contacts, accounts, and leads, configure the
applicable record layout in Salesforce CRM.").

  2. Check your security settings in Salesforce CRM.
    1. Confirm you have permissions selected for **View Setup and Configuration**.
    2. Set **Permitted Users** to **All users may self-authorize**.
    3. Under **OAuth Policies** , set **Refresh token policy** to **Refresh token is valid until revoked**.
  3. In Personalization, select **Third Party > Integration Setup**.
  4. Select **Salesforce CRM**.
  5. Check the status of the last synchronization job in the Status Message section. Review the status message. Click the status message to see details, if available.

Message details can include references to the CRM Jobs. You can find more
information about the execution of those jobs in your Salesforce CRM
environment.

  6. If the error detail includes any of the following error messages, complete the steps that follow to resolve the error:

Error | Description  
---|---  
Error refreshing Salesforce OAuth token | Token validity expired  
Error refreshing Salesforce OAuth token | Expired access/refresh token  
Error refreshing Salesforce OAuth token | inactive user  
INSUFFICIENT_ACCESS | Use of the Metadata API requires a user with the ModifyAllData permission  
  
  7. In Salesforce CRM, ensure the profile of the user establishing the OAuth connection has the ModifyAllData permission. This permission is necessary for Personalization to create custom fields using the Metadata API.
  8. Select **Setup** | **Manage Apps** | **Connected Apps**.
  9. Edit the Personalization connected app (your integration can be named differently).
    1. In OAuth policies, confirm **Permitted Users** is set to **All users may self-authorize** , and that **Refresh Token Policy** is set to **Refresh token is valid until revoked**. Make any necessary changes and click **Save**.
    2. At the top of the page next to your name, select **Setup**.
    3. Under **Build** , select **Create** | **Apps**.
    4. Under **Connected Apps** , click the name of the Personalization app. Don’t click **Edit** or **Manage**.
  10. In Personalization, select **Third Party** | **Integration Setup**.
  11. Select **Salesforce CRM**.
  12. Expand **Connect to Salesforce**.
  13. Copy the **Consumer Key** and the **Consumer Secret** from Salesforce CRM to Personalization.
  14. Click **Establish Connection**.
  15. Click **Synchronize Now**.

