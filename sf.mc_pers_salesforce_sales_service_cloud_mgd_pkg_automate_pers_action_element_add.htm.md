

# Add the Personalization Data Action Element to a Flow

Create an action element that maps how to send data to a specific
Personalization dataset after changes to a record occur.

### Required Editions and User Permissions

Available in: Premium edition  
---  
  
  

Permissions Needed  
---  
To add an Action element to a flow: | A role with permissions to access and work with action flows  
  
Before adding the Personalization Data Action Element to a flow, make sure to
set up your environment as described in [Personalization for Sales and Service
Cloud Integration
Setup](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_prereqs.htm&language=en_US&type=5
"Before configuring Personalization experiences, make sure to set up your
environment by completing these prerequisites in order.").

Make sure to provide non-administrator users with proper Apex class access
permissions for working with the Personalization Data Action flow element. For
more information, see [Set Apex Class Access from
Profiles](https://help.salesforce.com/s/articleView?id=sf.users_profiles_apex_access.htm&language=en_US&type=5).

When adding the Personalization data action element to a flow, also keep the
following in mind:

  * To save the action element, you must map a **Value** and **Attribute** pair for at least one Identity.
  * Mapping any **Value** and **Attribute** pairs for user attributes or profile objects is optional.
  * Values are sourced from Sales or Service Cloud. Value data is sent to its associated Attribute or Object Type destination in Personalization when the flow is triggered. Attributes and object types are sourced from the Personalization dataset that you select.

  1. If you’re modifying an existing Record-Triggered flow, open Flow Builder, and then open the flow you want to modify.
  2. Under the Run Asynchronously branch of the flow, and after any other Get Records or Assignment elements, click the Add Element option (![161530f7-5fb4-4c6e-a394-48b0f06f3ae6]).
  3. Under **Interaction** , select the **Action** flow element.
  4. In the left pane, click **Personalization**.
  5. Click the **Action** field in the right panel and select the **Automate Data Sent for Personalization** action. 
  6. Give the new Action element a label. The element assigns an API Name value for the element.

![3e44d006-35f7-4845-8994-9e54973a2c3c]

  7. (Optional) Provide a description for the element.
  8. Provide an **Interaction Name**. This value identifies the flow action within Marketing Cloud Personalization and enables more streamlined segment creation based on events coming from Sales and Service Cloud.
  9. From the **Dataset** dropdown menu, select a Personalization dataset.
  10. In the **Identities** section, map Sales or Service Cloud values to their respective Personalization attributes. The identity value either resolves to an existing Named Individual Profile, or creates a New Named Individual profile. 

![bf4760d5-8969-4435-858d-1cb40324ebd7]

Note To view additional details about existing identities, or to add more, see
[Identity Types and
Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5
"Personalization’s identity system uses deterministic matching to create a
Unified Customer Profile for each of your customers. Specific identifiers,
called identity types, determine how to process web events, API events, and
channel events to identify users from various sources. Personalization
includes several built-in identity types, such as email address and customer
ID. If the built-in identity types don’t meet the needs of your organization,
you can create additional identity types.").

![baf8b775-c5c8-4a17-a9a8-50cf3aa17971]

  11. (Optional) In the **User Attributes** section, click **Add Attribute** , and then map Sales or Service Cloud values to their respective Personalization attributes.

To view more details about existing user attributes, or to add more, see
[Create a User Profile
Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_attributes_create.htm&language=en_US&type=5
"User profile attributes can collect data you can use in segmentation,
reporting, or with integrated third-party systems. For example, if you create
a form in Personalization, you can assign each field to an existing attribute.
Depending on the configuration of your dataset, the attributes can either
collect the data for reporting, or can write it to a third-party integrated
system.").

![99c3ddb3-c606-493a-b1f3-135e72b3f6e3]

  12. (Optional) In the **Profile Objects** section, click **Add Profile Object** , and then map Sales or Service Cloud ID values to their respective profile object types.

To view additional details about existing related Profile Objects and
Attributes or to add more, see [User Profile
Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object.htm&language=en_US&type=5
"Gain a deeper understanding of your users by creating user profile
objects.").

![b9e32ab5-3751-426c-8e21-0bc99e639bd2]

  13. (Optional) Add profile object attributes by mapping their Sales or Service Cloud values to their respective Personalization attributes.
  14. (Optional) If an Asynchronous Apex process handles the creation or update of records and fields that trigger the Record-Triggered Flow, select **Increase Batch Size** to change the batch processing limit from 25 to 100 records per transaction.

![2aca85f5-a3c7-464f-9054-01c9091a3aea]

Note This increased processing limit matches the Apex limit of 100 total
callouts (HTTP requests or web services calls) in a transaction. It improves
performance but results in the removal of runtime validation for datasets,
attributes, and profile objects. For more information, see the developer
documentation: [Apex Governor
Limits](https://developer.salesforce.com/docs/atlas.en-
us.250.0.salesforce_app_limits_cheatsheet.meta/salesforce_app_limits_cheatsheet/salesforce_app_limits_platform_apexgov.htm).

  15. Click **Done** to save your changes.

#### See Also

  * [Mapping Values From Sales and Service Cloud to Personalization](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_mgd_pkg_automate_mapping.htm&language=en_US&type=5 "Using the Personalization action element, you select a dataset to send Sales and Service Cloud data to. You can then map data from Sales and Service Cloud to identities, user attributes, and profiles to attributes or profile object types in the Personalization dataset.")
  * [Sales to Service Cloud Use Cases](https://help.salesforce.com/s/articleView?id=sf.mc_pers_use_case_sales_service.htm&language=en_US&type=5)

