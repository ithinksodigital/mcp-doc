

# Add the Affinities Component to a Contacts or Leads Page

Add the Affinities component to view affinity data from Marketing Cloud
Personalization for a lead or contact.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To add the Affinities component: | A role with Administrator permissions  
  
Before adding the Affinities component, set up your environment as described
in [Personalization for Sales and Service Cloud Integration
Setup](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_prereqs.htm&language=en_US&type=5
"Before configuring Personalization experiences, make sure to set up your
environment by completing these prerequisites in order.").

  1. Next to Setup, click the **App Launcher**.
  2. Select the Sales or Service app.
  3. Open a **Contact** or **Lead** record.
  4. Click the Setup icon and select **Edit Page**.
  5. In the Components pane, in the Custom section, drag the Affinities component onto the page.
  6. Select a unique User Identifier for identity lookup.

For example, the Phone Number identity type is valid for both home and
business phone number user identifiers.

  7. Select the Personalization identity type that matches the lead or contact’s User Identifier. 

For example, if you select **Email** as the user identifier, select **Email
Address** as the Personalization identity type.

  8. Select the dataset and default catalog object type that you want to view. 

The dataset name includes the catalog object type in parentheses.

  9. (Optional) Select the default settings for filters, such as Show By and Date Range.
  10. (Optional) Select the catalog objects that you want to hide from the contact or lead’s view.
  11. Click **Save** , and then click **Activate**.

For non-administrator users to view the Affinities component, enable access to
the `InteractionStudioService` Apex class. For more information, see [Class
Security](https://developer.salesforce.com/docs/atlas.en-
us.250.0.apexcode.meta/apexcode/apex_classes_security.htm).

#### See Also

  * [Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5 "Personalization’s identity system uses deterministic matching to create a Unified Customer Profile for each of your customers. Specific identifiers, called identity types, determine how to process web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. If the built-in identity types don’t meet the needs of your organization, you can create additional identity types.")
  * [Sales to Service Cloud Use Cases](https://help.salesforce.com/s/articleView?id=sf.mc_pers_use_case_sales_service.htm&language=en_US&type=5)

