

# Create a User Profile Attribute

User profile attributes can collect data you can use in segmentation,
reporting, or with integrated third-party systems. For example, if you create
a form in Personalization, you can assign each field to an existing attribute.
Depending on the configuration of your dataset, the attributes can either
collect the data for reporting, or can write it to a third-party integrated
system.

### Required User Permissions

Permissions Needed  
---  
To create user profile attributes: | A role with User/Account Profile > Create/Edit permissions  
  
Before you begin creating user profile attributes, we suggest learning more
about [Attribute Update
Logic](https://help.salesforce.com/s/articleView?id=sf.mc_pers_profile_attribute_update.htm&language=en_US&type=5
"You can use multiple sources to update attributes. Attributes retain values
from authenticated sources such as ETL or Channel: Server \(/authevent API\)
over lower priority sources, such as the web.").

  1. From the main navigation, select **Settings** | **Attributes**.
  2. On the **User Attributes** tab, click **New Attribute**.
  3. Enter a **Name** for the attribute.

![e7e71cef-56f0-47a9-99e0-9bd9cc9d63f7]

Note You can’t change the name after you save the attribute. User profile
attributes and account profile attributes can’t have the same name.

  4. Enter a **Label** that describes the attribute. The label appears in the Unified Customer Profile.
  5. Select the **Type** for the attribute.

![5565408e-fbfd-4f11-abd6-05023b896050]

Note Identity attributes must be strings.

  6. Select an option from the **Classification Override** dropdown:

Item | Description  
---|---  
Sensitive | The attribute displays only to admins or people with a role that includes User/Account Profile > View Sensitive permissions, and you can’t use the attribute in a campaign. People with lesser permissions see asterisks instead of sensitive values on the Unified Customer Profile and segment lists. Additionally, email address fields (with a name of "emailAddress") aren’t searchable.  
Personally Identifiable | Anyone can view the attribute, but you can’t use the attribute in a campaign.The built-in identity types contain personally identifiable data, so their attributes should use this classification.  
Nonsensitive | Anyone can view the attribute, and you can use the attribute in a campaign.  
  
  7. If applicable, select the **Identity Type** for the attribute.
  8. To save the attribute, click the checkmark icon.
  9. Create additional attributes as necessary.

For the maximum number of user profile attributes per dataset, see
[Personalization
Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_limits.htm&language=en_US&type=5
"Learn about the limits and capabilities in Marketing Cloud
Personalization.").

#### See Also

  * [Attribute Update Logic](https://help.salesforce.com/s/articleView?id=sf.mc_pers_profile_attribute_update.htm&language=en_US&type=5 "You can use multiple sources to update attributes. Attributes retain values from authenticated sources such as ETL or Channel: Server \(/authevent API\) over lower priority sources, such as the web.")

