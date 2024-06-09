

# Configure an API Token for Personalization Experiences

You need an API token when integrating Marketing Cloud Personalization with
Sales and Service Cloud. Use API tokens to authenticate and authorize all API
requests to Personalization's REST API.

### Required User Permissions

Permissions Needed  
---  
To configure an API token: | A role with Administrator permissions  
  
  1. Log in to Personalization.
  2. From the bottom section of the main navigation, select **Security** | **API Tokens**.
  3. Click **Create Token**.
  4. Select only these permissions—**Can access API** , **Can send events** , and **Is enabled.**

![04ced812-0a8b-4170-8769-f1fe9ed6ab23]

Note Personalization doesn’t currently support restricting API tokens to
specific datasets for the Personalization for Sales and Service Cloud managed
package. Specifying any datasets in the **Restrict to Specific Datasets**
field disables the API token for use with the Sales and Service Cloud manage
package.

  5. Click **OK**. A dialog box opens stating that the token has been created and shows the Download API Key Credentials dialog appears. Don’t close this dialog box. 
  6. From the dialog box, copy the **API Key ID** and the **API Key Secret**.
  7. Click **Download CSV File** and store the file in a secure location.

![df152788-fa3e-4efc-b567-74bd174a4bd4]

Note These values can be used to access your data in Personalization, so
download and store them securely. After you close this dialog, you can’t
access these values again.

  8. After you copy and download the API key ID and API key secret, click **Close** to close the dialog.

Previous

**[Install Personalization for Sales and Service
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_install.htm&language=en_US&type=5
"Download the Personalization for Sales and Service Cloud managed package from
AppExchange to access real-time product recommendations and customer
affinities and events directly in Sales and Service Cloud. Also get near real-
time Sales and Service Cloud data in the Personalization platform.")**

Next

**[Create a Named Credential for Personalization
Experiences](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_named_credential.htm&language=en_US&type=5
"Create a named credential to establish a trusted connection between
Salesforce CRM and Marketing Cloud Personalization.")**

