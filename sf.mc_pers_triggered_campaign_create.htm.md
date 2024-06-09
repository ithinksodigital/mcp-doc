

# Create a Triggered Campaign

Use a triggered campaign to launch a journey when a specific action or event
occurs. For example, send a promotion to a shopper who spent time viewing a
product but didn’t purchase. You can recommend unread articles or products to
a visitor who has spent more than 5 minutes reading about a topic. You can
remind new users to complete onboarding steps, or alert sales reps when target
prospects spend a certain amount of time on your site. When creating a
triggered campaign, you can define when to trigger the campaign, which users
to target, and which experiences to deliver.

### Required User Permissions

Permissions Needed  
---  
To create a triggered campaign: | A role with Campaigns Create/Edit permissions  
To publish a triggered campaign: | A role with Campaigns Publish/Delete permissions  
  
Before you create a triggered campaign, complete the required setup steps, and
configure a triggered campaign template. A triggered campaign requires a
triggered template. See [Requirements for Creating Triggered
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_prerequisites.htm&language=en_US&type=5
"To create a triggered campaign, you must configure components in Contact
Builder, Journey Builder, and Personalization.").

  1. From the main navigation, select **Triggered** | **Triggered Campaigns**.
  2. Click **New Campaign** and name your campaign.
  3. Select the trigger type and related options. For more information, see [User Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_user.htm&language=en_US&type=5 "A user trigger activates a campaign based on user behavior.") and [Catalog Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_catalog.htm&language=en_US&type=5 "A catalog trigger activates a campaign based on updates or changes to item data in your catalog. The trigger activates after a change in your catalog, but what drives the trigger is the amount of time the user views an item before the catalog change occurs."). 
  4. (Optional) For some trigger types, you can add a catalog filter to narrow campaign qualification based on criteria, such as product price, average rating, features, or style. 
  5. (Optional) For some trigger types, you can add a behavior filter to narrow campaign qualification based on user behaviors, such as adding a product to favorites or to the cart. 
  6. To override the default dataset setting for how many times an item appears during a campaign, select **Trigger Item Frequency**. 
  7. To control how many times a triggered campaign activates for a profile, for Campaign Frequency Limits, add a **New Frequency Limit** time frame, and a maximum number of triggers. 
  8. To schedule when the campaign triggers for qualified users, click **Add Delay** and configure these settings as needed. 

Setting | Description  
---|---  
Delay Send | Delays sending the campaign after the trigger activates based on the amount of time entered.  
Send during specific days and hours | Sends the trigger during the specified time. You can select multiple days and times.  
Use your browser’s current timezone offset | The days and hours that you choose are based on your own time zone.  
Use the recipient’s timezone | The days and hours that you choose are based on the time zone of each campaign recipient’s device.  
  
  9. To add a campaign targeting rule, click **Add Rule** and select the category and rule. You can use AND logic to add multiple rules. For more information, see [Rule Categories](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_rule.htm&language=en_US&type=5 "There are a variety of rules that you can add for campaign targeting and rule-based campaign experiences when you create or edit a campaign.").
  10. Select either **A/B Test** or **Rule Based Test** as the campaign type.
  11. If you select **A/B Test** , enter a percentage for the experience and control groups. For more information, see [A/B Test Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_a_b_test.htm&language=en_US&type=5 "When creating an A/B test campaign, you include multiple experiences, and assign each experience a percentage of traffic. A/B tests give you flexibility and control over how Personalization distributes traffic and which users see which experiences.").

Users must qualify for an experience to be included in the control group.
Users in the control group aren’t sent to the journey.

  12. If you select **Rule Based Test** , enter a percentage for the control group, click **Add Rule** , and select the category and rule for the experience. For more information, see [Rule Categories](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_rule.htm&language=en_US&type=5 "There are a variety of rules that you can add for campaign targeting and rule-based campaign experiences when you create or edit a campaign.").

You can also add experiences by clicking the clone icon or **Experience+** in
the left navigation.

You can add multiple rules, but visitors must satisfy all the rules,
regardless of the order, to qualify for the experience.

  13. For each experience, select the triggered campaign template to use.
  14. For each experience, click **Add to Journey Builder** and configure the API event and Marketing Cloud Engagement contact key to ensure that users who qualify are added to the journey.
  15. Save your campaign, and publish it when you’re ready to go live.

In Contact Builder, update the Marketing Cloud Engagement data extension to
include fields for any options you added in the triggered template for each
campaign experience.

#### See Also

  * [User Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_user.htm&language=en_US&type=5 "A user trigger activates a campaign based on user behavior.")
  * [Catalog Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_catalog.htm&language=en_US&type=5 "A catalog trigger activates a campaign based on updates or changes to item data in your catalog. The trigger activates after a change in your catalog, but what drives the trigger is the amount of time the user views an item before the catalog change occurs.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")
  * [Triggered Campaigns Use Cases](https://help.salesforce.com/s/articleView?id=sf.mc_pers_use_case_triggered.htm&language=en_US&type=5 "Drive impact through Triggered Campaigns, passing real-time information to Marketing Cloud Engagement. Check out these example personalization use cases that other customers have used in triggered campaigns.")

