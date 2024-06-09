

# Configure Anonymous Data Export to Data Cloud

By default, Marketing Cloud Personalization sends only named users and events
to Data Cloud. You can configure Personalization to send anonymous user and
event data as well.

### Required User Permissions

Permissions Needed  
---  
To configure anonymous data export: | A role with Administrator permissions  
  
  1. Before you can share anonymous users with Data Cloud, you must set up the Marketing Cloud Personalization Connector. For more information, see [Set Up a Connection to Marketing Cloud Personalization](https://help.salesforce.com/s/articleView?id=sf.c360_a_set_up_interaction_studio_connector.htm&language=en_US&type=5) and [Marketing Cloud Personalization Connector](https://help.salesforce.com/s/articleView?id=sf.c360_a_interaction_studio_connector.htm&language=en_US&type=5) in Data Cloud Help. 
  2. Log in to Personalization as an administrator.
  3. From the bottom section of the main navigation, select **Settings > General Setup**.
  4. Click **Advanced Options**.
  5. Scroll down and select **Sync Anonymous Users to Salesforce CDP**.
  6. Click **Save**.

![741e35d3-8b66-484b-bb8f-591f91d28eee]

Note In Data Cloud, you must configure party identification for anonymous
events to merge to a known profile.

