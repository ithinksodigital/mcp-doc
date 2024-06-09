

# Create an API Token

Marketing Cloud Personalization uses API tokens to authenticate and authorize
all API requests to Personalization's REST API.

### Required User Permissions

Permissions Needed  
---  
To create an API token: | A role with Administrator permissions  
  
  1. From the bottom section of the main navigation, select **Security > API Tokens**. 
  2. Click **Create Token**.
  3. To allow the token to access the API, select **Can access API**.
  4. To allow the token to send events, select **Can send events**.
  5. To restrict access to specific datasets in your Personalization account, select the datasets from the **Select datasets** field. Otherwise, the token applies to all current and future datasets in your account.
  6. Add any **Notes** about the token as necessary.
  7. To define the IP addresses that can use the token, enter the IP addresses into the IP Accept List field and separate them with commas. When configured, requests that originate from addresses not on this list are rejected.
  8. Click **OK**.
  9. A dialog appears so you can access the API Key ID and API Key Secret, which function like a username and password in an API request. 

![4fd0e50d-15f1-4f1f-8583-5940ecd3ebcd]

Note These values can be used to access your data in Personalization, so
download and store them securely. After you close this dialog, you can’t
access these values again.

