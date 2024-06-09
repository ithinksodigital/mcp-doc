

# Set Up Integration with Salesforce CRM

Complete these steps to set up the integration between Marketing Cloud
Personalization and Salesforce CRM.

### Required User Permissions

Permissions Needed  
---  
To integrate with Salesforce CRM: | A role with Administrator permissions  
  
  1. Log in to Personalization as an administrator.

For more information, see [Log In To Personalization from Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_login.htm&language=en_US&type=5
"Access Marketing Cloud Personalization from Marketing Cloud Engagement.").

  2. From the main navigation, select **Third-Party > Integration Setup**.
  3. Select **Salesforce CRM**.
  4. On the **Setup** tab, expand the **Connect to Salesforce** section.
  5. Copy the **Callback URL**.

Don’t log out of Personalization.

  6. Open Salesforce CRM in a new browser window. Log in as an administrator.

![c143f1e7-a85e-4c59-a8aa-c67eefac78af]

Note The user profile for this administrator account must have the **API
Enabled** permission enabled.

  7. Select **Setup**.
  8. In the **Platform Tools** section, select **Apps > Apps Manager**.
  9. Click **New Connected App**.
  10. In **Basic Information** , complete the required fields.

Field | Description  
---|---  
**Connected App Name** | Enter a label, such as `Marketing Cloud Personalization`.  
**API Name** | Personalization automatically prefills.  
**Contact Email** | Enter your email address.  
  
  11. In **API (Enable OAuth Settings)** , select **Enable OAuth Settings**.
  12. In the **Callback URL** field, paste the callback URL you copied from Personalization.
  13. Select the following **OAuth Scopes** :

OAuth Scopes  
---  
**Manage user data via APIs (api)**  
**Access the identity URL service**  
**Perform requests at any time**  
  
  14. If **Require Proof Key for Code Exchange (PKCE) Extension for Supported Authorization Flows** is visible and selected, be sure to deselect it.

This setting, if available in your org, must be disabled for this Connected
App.

  15. Click **Save**.
  16. In Salesforce CRM, in the **Connected App Name: Marketing Cloud Personalization** page, scroll down to the **API (Enable OAuth Settings)** section. 
  17. Next to **Consumer Key and Secret** , click **Manage Consumer Details** and configure the following settings:

Field | Description  
---|---  
**Consumer Key** | Copy this key from Salesforce CRM to the same field in Personalization in **Third Party > Integrations > Salesforce CRM**.  
**Consumer Secret** | Click **Click** and then copy the secret from Salesforce CRM to the same field in Personalization in **Third Party > Integrations > Salesforce CRM**.  
  
  18. If you’re connecting to a Salesforce CRM sandbox account, in Personalization, select **Connect to a sandbox**.
  19. Under **Advanced Options** , select the **For Salesforce accounts that cannot otherwise be matched to Interaction Studio, obtain account IDs from matched Salesforce contacts** option.

This option pulls account IDs from Salesforce CRM instead of Personalization
so that you can match users with the same contact name when the account names
aren’t exact matches.

  20. Click **Save**.
  21. Click **Establish Connection** to create the connection between Personalization and Salesforce CRM.
  22. If prompted, log in to your Salesforce CRM account.
  23. If prompted, click **Allow** to allow Personalization to access information in Salesforce CRM.

Next, determine which data you want to share between Personalization and
Salesforce CRM. For more information, see [Plan Data Sharing Between
Personalization and Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization.htm&language=en_US&type=5
"Before initializing data sharing, decide what data you want to exchange
between Salesforce CRM and Personalization and how you want to match data for
merging. After initialization, Marketing Cloud Personalization shares data
with Salesforce CRM on a nightly basis. Contacts and accounts are shared
automatically, but leads sharing is optional.").

#### See Also

  * [ _Salesforce CRM Help_ : Connected Apps](https://help.salesforce.com/s/articleView?id=sf.connected_app_overview.htm&language=en_US&type=5)

