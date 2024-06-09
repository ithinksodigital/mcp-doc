

# Configure Server-Side Campaigns for Next-Best-Recommendations

To use the next-best recommendations component, you must configure server-side
campaigns in Marketing Cloud Personalization. A developer must create the
server-side template.

### Required User Permissions

Permissions Needed  
---  
To configure server-side campaigns: | A role with Administrator permissions  
  
  1. Log in to Personalization.
  2. Download and publish the Server-Side CRM Recommendations template.

![9a3d0544-b2d1-4149-8913-a7f911a1df2a]

Note Use the template for any new campaigns. It’s important that you modify
only the number of items that return, or the recommendation type, such as
Product, Blog, or Article. Any other modifications can prevent the component
from rendering a response. If you have existing recommendations campaigns
published that use the Server-Side classic interface, they’ll continue to
work.

  3. From the **Channels & Campaigns** section of the main navigation, select **Server-Side > Server-Side Campaigns**.
  4. Click **New Campaign**.
  5. Apply the Sales and Service Cloud Connector - Next Best Recommendations template and fill in the associated values.

Setting | Description  
---|---  
**Datafield** | Map the datafield value to what you have entered in the recommendations component configuration in the sales/service interface. The default sales/service value is `recs`, but you can change it. For example, if you have two recommendation components on your contact/lead record page and want to target different campaigns for each, a campaign only renders in a component that has a matching datafield value. If two campaigns share a datafield value and a user qualifies for both based on campaign targeting logic, both campaigns render in the same CRM component.  
**Recipe** | Select your desired recipe from the dropdown of published recipes. If no options display, there aren’t any published recipes available for the item type that you’re trying to recommend.  
  
  6. Apply any targeting logic and adjust the campaign control setting. If you want decisions to always return, make sure there’s no control percentage applied.
  7. Click **Save** , and then publish the campaign.

![c5b4fa85-3a92-4f4a-ad33-59888825515d]

Note Impression and click data isn’t currently sent to Personalization from
Salesforce CRM.

  8. In Salesforce CRM, select **Sales** or **Service Cloud**.
  9. Open a **Contact** or **Lead** record.
  10. Select **Setup > Edit Page**.
  11. Select the **Next Best Product** component that you've added to the page and configure the following settings:

Setting | Description  
---|---  
**User Identifier** | Enter the unique user identifier that matches the user identifier in Personalization for identity lookup. Typically, the identifier is **Email** , but you can change this in your dataset.  
**Identity Type** | Enter the Personalization identity type that matches the lead or contact’s user identifier. For example, if you select Email as the user identifier, select Email Address as the Personalization identity type.  
**Dataset** | Select the Personalization dataset where you've built and configured your server-side campaign.   
**Datafield** | Enter the value that you entered in the **Datafield** text box from your server-side campaign.  
**Action Name** | Enter a value that is meaningful to you. This value appears in the Event Stream.  
**Channel** | Select **Server**.  
**Remove Image** | Select this option to hide recommended item images on the contact or lead record.  
**Remove Details Button** | Select this option to hide recommended item details on the contact or lead record.  
**Remove Description** | Select this option to hide recommended item descriptions on the contact or lead record.  
  
  12. Click **Save**.
  13. To have multiple Next Best Product components display on the contact or lead page, repeat these steps.

#### See Also

  * [Add Next-Best Components to a Contacts or Leads Page](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_component.htm&language=en_US&type=5 "Add components to view next-best offers or recommendations for a contact or lead.")
  * [Create a Server-Side Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign_create.htm&language=en_US&type=5 "You can create server-side campaigns to personalize experiences across multiple channels with a single campaign.")
  * [ _Developer Documentation_ : Server-Side Templates](https://developer.salesforce.com/docs/marketing/personalization/guide/server-side-campaigns-templates.html)
  * [ _Developer Documentation_ : Sales/Service Cloud Connector - Next Best Recommendations Template](https://developer.salesforce.com/docs/marketing/personalization/guide/server-side-next-best-recs-template.html)

