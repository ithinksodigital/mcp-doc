

# Create a Mobile Data Campaign

Create Mobile Data campaigns so your iOS and Android apps can process
Personalization campaign data. Personalization triggers campaigns and delivers
the data to your app.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create or edit Mobile Data campaigns: | A role with Campaign Create/Edit permissions  
To publish or delete Mobile Data campaigns: | A role with Campaign Publish/Delete permissions  
  
  1. In the **Channels & Campaigns** section of the main navigation, select **Mobile** | **Mobile Data Campaigns**.
  2. Click **NEW CAMPAIGN.**
  3. In the **Target** field, enter the app content zone that matches the app code. For more information, see the developer documentation for [iOS](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-ios-sdk/mobile-data-campaigns.html) and [Android](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-android-sdk/v1.3.0/mobile-data-campaigns.html) Mobile Data Campaigns.
  4. To define the data payload, click **Add New** to insert a new data item.
  5. Enter a static string identifier for the **Name** of the data item.
  6. Select the **Type** of data that you want to assign to the data item.

Type | Description  
---|---  
**Text** | The value is a JSON string.  
**Number** | The value is a JSON number.  
**Promoted Content** | The value is defined by the promoted content in Message Rules. For more information, see the developer documentation for [Add Mobile Message Targeting Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_message_targeting_rules.htm&language=en_US&type=5 "After you create a Mobile In-App Message or Mobile Data campaign, you can add message rules and promote content in Message Rules. Message rules control when a mobile in-app message shows for a visitor. For example, show the message when a visitor takes a specific action. Or only show the message a certain number of times per visit, during a specific time period, or all of the time. Use Promoted Content to promote a specific item or multiple items either by selecting the item or by using Einstein Recipes algorithms or Einstein Decisions AI.").  
  
  7. Enter a static or dynamic **Value** for the data item for Type you selected. To insert dynamic content queries, select the **Value** entry, click the **Dynamic+** dropdown, and select the dynamic value. Text and Number data items can send dynamic values, such as username, email address, or custom user attributes. 

Text and Number types can use Dynamic Message Content (DMC) and Advanced
Dynamic Message Content (ADMC) syntax. For information about ADMC, see
[Salesforce Developer Documentation: ADMC
Reference](https://developer.salesforce.com/docs/marketing/personalization/guide/advanced-
dynamic-message-content.html)

![0ad0a7de-ebe0-4011-b85c-e06adc310d84]

Note If Personalization can’t populate the dynamic value, the experience can’t
trigger, and, in some cases, the campaign can’t display. You can use the
#field syntax to provide a fallback value. See [Add a Fallback Value for
Dynamic
Content](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_dynamic_values_add_fallback_value.htm&language=en_US&type=5
"If dynamic content doesn’t appear because there’s no correlating value, you
can add a fallback value that shows instead.").

  8. Repeat adding new data items until you define all items in the payload.
  9. To configure promoted content, set the **Type** to **Promoted Content**. Then set the **Value** to one of the following:

Option | Description  
---|---  
**$items** | Returns all applicable items as a JSON array.  
**$item** | Returns one applicable item as a JSON object.  
  
  10. Configure **Promoted Content** in **Message Rules**.
  11. If you include more than one campaign experience, select one of these options:

Option | Description  
---|---  
**Copy To All** | Copies a data item value across all campaign experiences.  
**Delete** | Removes a data item from all campaign experiences.  
  
  12. Incorporate targeting rules. For more information, see [Add Mobile Message Targeting Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_message_targeting_rules.htm&language=en_US&type=5 "After you create a Mobile In-App Message or Mobile Data campaign, you can add message rules and promote content in Message Rules. Message rules control when a mobile in-app message shows for a visitor. For example, show the message when a visitor takes a specific action. Or only show the message a certain number of times per visit, during a specific time period, or all of the time. Use Promoted Content to promote a specific item or multiple items either by selecting the item or by using Einstein Recipes algorithms or Einstein Decisions AI.") and [Add Mobile Campaign Targeting Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_targeting_rules.htm&language=en_US&type=5 "Campaign-wide rules control the visibility of mobile campaigns based on things like segments, visit count and duration, and user actions. Set rules at the campaign level when you want to holistically control how a campaign displays.").

#### See Also

  * [ _Developer Documentation_ : iOS Mobile Data Campaigns](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-ios-sdk/mobile-data-campaigns.html)
  * [ _Developer Documentation_ : Android Mobile Data Campaigns](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-android-sdk/v1.3.0/mobile-data-campaigns.html)

