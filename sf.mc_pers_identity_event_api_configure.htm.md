

# Configure the Identity System for the Event API

Set up the identity system for the Event API.

### Required User Permissions

Permissions Needed  
---  
To configure the identity system: | A role with Administrator permissions  
  
Before you start, make sure your API request includes “Server” as the channel
parameter nested beneath the source parameter.

![2e42c1bc-4ea9-4726-aa0a-229a1c997998]

Note The channel parameter is case-sensitive.

  1. To send identity types as user attributes:
    1. Don’t include the user ID parameter in your API request.
    2. Include identity types as user attributes.
  2. To select an identity type and send it as the user ID parameter, and send other identity types as user attributes:
    1. From the main navigation, select **Settings** | **General Setup**.
    2. Expand **Advanced Options**.
    3. From the **Select the Identity attribute to use as the Server Side events Identity** dropdown, select the identity type.

![48e766f9-3755-467c-8574-d67666ca2d24]

Note If you have active campaigns, changing this setting can impact the
content that appears for those campaigns.

    4. Click **Save**.
    5. Include the selected identity type as the user ID parameter in your API request.
    6. Include other identity types as user attributes.

#### See Also

  * [ _Developer Documentation_ : Marketing Cloud Personalization Event API](https://developer.salesforce.com/docs/marketing/personalization/guide/event-api.html)

