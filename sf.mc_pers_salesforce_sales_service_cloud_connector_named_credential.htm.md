

# Create a Named Credential for Personalization Experiences

Create a named credential to establish a trusted connection between Salesforce
CRM and Marketing Cloud Personalization.

### Required Editions and User Permissions

Available in: Premium edition  
---  
  
  

Permissions Needed  
---  
To create named credentials: | View Setup and Configuration  
  
![156ee269-c7f9-4808-9716-1ed82e549885]

Note If you already have an existing Personalization named credential, you
don’t need to create another. However, to use the existing credential, ensure
that:

  * The API token you are using is not dataset restricted. Personalization doesn’t currently support restricting API tokens to specific datasets for the Personalization for Sales and Service Cloud managed package.
  * You update the URL field with the most recent Gears URL.

To create a named credential for Personalization experiences:

  1. From Setup, enter `Named Credentials` in the Quick Find box, then select **Named Credentials**.
  2. Click **Named Credentials**.
  3. From the dropdown menu in the upper right of the Named Credentials tab, select **New Legacy**.
  4. Complete the fields using the information in this table.

Field | Description  
---|---  
Label | `Interaction_Studio_Creds`  
Name | `Interaction_Studio_Creds`  
URL | Use the base URL of your Personalization account, such as https://<companyname>.evergage.com. You can find it by selecting **Gears** | **Gears** and viewing the URL in the address bar of your browser.If your instance isn’t us-1, you must include your instance in the URL string.  
Authentication:  
Certificate | Leave this field blank.  
Identity Type | Select **Named Principal**.  
Authentication Protocol | Select **Password Authentication**.  
Username | Paste the API key ID that you copied.  
Password | Paste the API key secret that you copied.  
Callout Options:  
Generate Authorization Header | Select this option.  
Allow Merge Fields in HTTP Header | Don’t select this option.   
Allow Merge Fields in HTTP Body | Don’t select this option.  
Outbound Network Connection | Leave the field blank.  
  
  5. Click **Save**.

Previous

**[Configure an API Token for Personalization
Experiences](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_api_token.htm&language=en_US&type=5
"You need an API token when integrating Marketing Cloud Personalization with
Sales and Service Cloud. Use API tokens to authenticate and authorize all API
requests to Personalization's REST API.")**

