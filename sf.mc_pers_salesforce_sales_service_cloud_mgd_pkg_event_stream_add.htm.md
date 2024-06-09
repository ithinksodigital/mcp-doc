

# Add the Customer Event Stream Component to a Contacts or Leads Page

Watch your customers interact with your business in real-time as well as view
historical activities right on a Contacts or Leads page with the event stream
component of the Personalization managed package. Events are based on the data
provided by the Interactions SDK or Sitemap. For custom events, you can view
event name, URL (if applicable), timestamp, and channel.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To add the Event Stream component: | A role with Administrator permissions  
  
Before adding the Event Stream component, set up your environment as described
in [Personalization for Sales and Service Cloud Integration
Setup](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_prereqs.htm&language=en_US&type=5
"Before configuring Personalization experiences, make sure to set up your
environment by completing these prerequisites in order.").

![9e710f73-62c6-481a-bccc-2e6a82835b07]

Note In the event stream, inventory status reflects the status at the time of
the event. To view inventory status, make sure to specify the inventory count
in the sitemap. Inventory count is stored in the product catalog. For more
information about sitemaps, including catalog information examples, see the
developer documentation [Getting Started with Site
Mapping](https://developer.salesforce.com/docs/marketing/personalization/guide/sitemapping-
getting-started.html?q=sitemap).

  1. From the App Launcher, find and select the Sales or Service app.
  2. Open a contact or lead record.
  3. From Setup, select **Edit Page**.
  4. In the Components pane, in the Custom section, drag the Event Stream component onto the page.
  5. Select a unique user identifier for identity lookup.
  6. Select the Personalization identity type that matches the lead or contact’s User Identifier. 

For example, if you select **Email** as the user identifier, select **Email
Address** as the Personalization identity type.

  7. Select the dataset that you want to view. 
  8. Enter the number of events to show, and select the event types that you want to hide.
  9. Click **Save** , and then click **Activate**.

To let non-admin users view the Event Stream component, grant access to the
`InteractionStudioService` Apex class. For more information, see [Class
Security](https://developer.salesforce.com/docs/atlas.en-
us.250.0.apexcode.meta/apexcode/apex_classes_security.htm).

