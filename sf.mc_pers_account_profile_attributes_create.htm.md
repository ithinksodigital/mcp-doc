

# Create an Account Profile Attribute

Account profile attributes can collect data you can use in segmentation,
reporting, or with integrated third-party systems. For example, if you create
a form in Personalization, you can assign each field to an existing attribute.
Depending on the configuration of your dataset, the attributes can either
collect the data for reporting, or can write it to a third-party integrated
system.

### Required User Permissions

Permissions Needed  
---  
To create account profile attributes: | A role with User/Account Profile > Create/Edit permissions  
  
  1. Before you begin, learn about [Attribute Update Logic](https://help.salesforce.com/s/articleView?id=sf.mc_pers_profile_attribute_update.htm&language=en_US&type=5 "You can use multiple sources to update attributes. Attributes retain values from authenticated sources such as ETL or Channel: Server \(/authevent API\) over lower priority sources, such as the web.").
  2. From the bottom section of the main navigation, select **Settings > Attributes**.
  3. Click the **Account Attributes** tab.
  4. Click **New Attribute**.
  5. Enter a **Name** for the attribute.

![b16b42aa-755a-4175-85fd-2fb4c5e062be]

Note You can’t change the name after you save the attribute. Account profile
attributes and user profile attributes can’t have the same name.

  6. Enter a **Label** that describes the attribute.

![72f7096e-c9ea-4ad2-95a4-9572b76a26d1]

Note The label appears in the Unified Account Profile.

  7. Select the **Type** for the attribute.
  8. Select an option from the **Classification Override** dropdown:

Attribute | Description  
---|---  
**Sensitive** | The attribute displays only to admins or people with a role that includes User/Account Profile > View Sensitive permissions, and you can’t use the attribute in a campaign. People with lesser permissions see asterisks instead of sensitive values on the Unified Account Profile and segment lists. Additionally, email address fields (with the name of "emailAddress") aren’t searchable.  
**Personally Identifiable** | Anyone can view the attribute, but you can’t use the attribute in a campaign.  
**Nonsensitive** | Anyone can view the attribute, and you can use the attribute in a campaign.  
  
  9. To save the attribute, click the checkmark icon.
  10. Create additional attributes as necessary.

![3e931492-e7ff-40ed-adbc-4f96d6fabb45]

Note The maximum number of account profile attributes per dataset is 100.

#### See Also

  * [Attribute Update Logic](https://help.salesforce.com/s/articleView?id=sf.mc_pers_profile_attribute_update.htm&language=en_US&type=5 "You can use multiple sources to update attributes. Attributes retain values from authenticated sources such as ETL or Channel: Server \(/authevent API\) over lower priority sources, such as the web.")

