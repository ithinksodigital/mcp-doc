

# Generate API Tokens to Authorize Data Changes

Authorize all data changes by creating a token for use in API calls. You
generate the API token with the User Look-Up and Deletion API. This API
exports individual user data to satisfy right of access requests.

### Required User Permissions

Permissions Needed  
---  
To create API tokens: | Administrator access  
  
  1. Select the production dataset associated with the individual that you want to edit.
  2. On the main navigation, select **Security** | **API Tokens**.
  3. Click **Create Token** , and optionally add notes about the token.
  4. Keep the default permissions.

**Can access API** isn’t selected. **Can send events** is selected.

  5. If you want to restrict access to specific datasets in your account, add them in Restrict to Specific Datasets. If you don’t restrict any datasets, the token applies to all current and future datasets in your account.
  6. To limit which IP addresses can use the token, add them to the IP Accept List. The API rejects any requests that originate from addresses not on the accept list.
  7. Click **OK**.
  8. To access the token value, on the API Tokens screen, double-click the token. The value is in the **Editing API Token** field.
  9. To use an API to retrieve and delete user data in Personalization, see [User Look-Up and Deletion API](https://developer.salesforce.com/docs/marketing/personalization/guide/user-look-up-deletion-api.html).

