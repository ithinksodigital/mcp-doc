

# Configure Server-Side Campaigns for Next-Best-Offers

To use the next-best offers component, you must configure server-side
campaigns in Marketing Cloud Personalization. A developer must create the
server-side template.

### Required User Permissions

Permissions Needed  
---  
To configure server-side campaigns: | A role with Administrator permissions  
  
  1. Log in to Personalization.
  2. Download and publish the Server-Side CRM Einstein Decisions template.

![98842a13-2359-4f1b-b9ec-b020babe0d5f]

Note Use the template for any new campaigns. It’s important that you modify
only the number of items that return, or the offer type, such as Product,
Blog, or Article. Any other modifications can prevent the component from
rendering a response. If you have existing recommendations campaigns published
that use the Server-Side classic interface, they’ll continue to work.

  3. From the **Channels & Campaigns** section of the main navigation, select **Server-Side > Server-Side Campaigns**.
  4. Click **New Campaign**.
  5. Apply the Sales and Service Cloud Connector - Einstein Decisions template and fill in the associated values:

Setting | Description  
---|---  
**Asset Content Zone or Tag** | Select the content zone or tag that you want Einstein Decisions to use during the decision process, and define an optional fallback.  
**Datafield** | Map the **Datafield** value to what you have entered in the Next Best Promotion and Action component configuration in the sales/service interface. The default sales/service value is `promos`, but you can change it. For example, if you have two components on your contact/lead record page and want to target different campaigns for each, a campaign only renders in a component that has a matching datafield value. If two campaigns share a datafield value and a user qualifies for both based on campaign targeting logic, both campaigns render in the same CRM component.  
  
  6. Apply any targeting logic and adjust the campaign control setting. If you always want recommendations to return, make sure that there’s no control percentage applied.
  7. Click **Save** , and then publish the campaign.

![44d1b1b0-9116-48ab-99a0-17c6296da930]

Note Impression and click data isn’t currently sent back to Personalization
from Salesforce CRM.

  8. In Salesforce CRM, select **Sales** or **Service Cloud**.
  9. Open a **Contact** or **Lead** record.
  10. Select **Setup > Edit Page**.
  11. Select the **Next Best Promotion and Action** component that you've added to the page and configure the following settings.

Setting | Description  
---|---  
**User Identifier** | Enter the unique user identifier that matches the user identifier in Personalization for identity lookup. Typically, the identifier is **Email** , but you can change this in your dataset.  
**Identity Type** | Enter the Personalization identity type that matches the lead or contact’s user identifier. For example, if you select Email as the user identifier, select Email Address as the Personalization identity type.  
**Dataset** | Select the Personalization dataset where you've built and configured your server-side campaign.  
**Datafield** | Enter the value that you entered in the **Datafield** text box from your server-side campaign.  
**Action Name** | Enter a value that is meaningful to you. This value appears in the Event Stream.  
**Channel** | Select **Server**.  
**Remove Image** | Select this option if you want to hide recommended item images on the contact or lead record.  
**Remove Details Button** | Select this option if you want to hide recommended item details on the contact or lead record.  
**Remove Description** | Select this option if you want to hide recommended item descriptions on the contact or lead record.  
  
  12. Click **Save**.

#### See Also

  * [Add Next-Best Components to a Contacts or Leads Page](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_component.htm&language=en_US&type=5 "Add components to view next-best offers or recommendations for a contact or lead.")
  * [Create a Server-Side Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign_create.htm&language=en_US&type=5 "You can create server-side campaigns to personalize experiences across multiple channels with a single campaign.")
  * [ _Developer Documentation_ : Server-Side Templates](https://developer.salesforce.com/docs/marketing/personalization/guide/server-side-campaigns-templates.html)
  * [ _Developer Documentation_ : Sales/Service Cloud Connector - Einstein Decisions Template](https://developer.salesforce.com/docs/marketing/personalization/guide/sales-service-cloud-connector-einstein-decisions.html)

