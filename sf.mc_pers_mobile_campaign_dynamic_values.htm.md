

# Use Dynamic Values in Mobile Campaigns

You can add dynamic values, such as the mobile app user’s name, location, and
email, to all mobile campaign types.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create or edit mobile campaigns: | A role with Campaign Create/Edit permissions  
  
Personalization supports dynamic message content and Advanced Dynamic Message
Content (ADMC) syntax. You can insert dynamic content into your mobile
campaign messages, and dynamic values are populated with the stored value for
the mobile app user in real time. For information about ADMC, see [Salesforce
Developer Documentation: ADMC
Reference](https://developer.salesforce.com/docs/marketing/personalization/guide/advanced-
dynamic-message-content.html).

If Personalization can’t populate a dynamic value, the experience can’t
trigger and, in some cases, the campaign can’t display. You can use the
`#field` syntax to provide a fallback value. See [Add a Fallback Value for
Dynamic
Content](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_dynamic_values_add_fallback_value.htm&language=en_US&type=5
"If dynamic content doesn’t appear because there’s no correlating value, you
can add a fallback value that shows instead.").

  1. Create a mobile campaign.
  2. Select the field you want to add the dynamic content to, such as **Title** , **Body** , or **Additional Data Values (not Keys)**.
  3. Click **Dynamic+** and select a value.
  4. Continue editing the campaign as necessary.
  5. Save your changes.

