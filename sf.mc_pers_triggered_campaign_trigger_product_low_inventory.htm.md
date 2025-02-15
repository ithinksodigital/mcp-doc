

# Product Low Inventory Trigger

Use this trigger to reach customers when a product they spent time viewing but
didn’t purchase has a low inventory. The user must have viewed the product for
a minimum amount of time within a specified number of days. Marketing Cloud
Personalization uses the minimum view time to filter out customers that look
at a product only for 1 second before they navigate away. The trigger checks
every hour for qualifying products that have an inventory count below the
configured threshold.

You can select this trigger type when you create a triggered campaign. For
more information, see [Create a Triggered
Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5
"Use a triggered campaign to launch a journey when a specific action or event
occurs. For example, send a promotion to a shopper who spent time viewing a
product but didn’t purchase. You can recommend unread articles or products to
a visitor who has spent more than 5 minutes reading about a topic. You can
remind new users to complete onboarding steps, or alert sales reps when target
prospects spend a certain amount of time on your site. When creating a
triggered campaign, you can define when to trigger the campaign, which users
to target, and which experiences to deliver.").

## Configuration Options

You can configure these options when you add a low-inventory trigger to a
campaign.

Option | Description  
---|---  
Low Inventory Count Threshold | The trigger is activated when the number of products in inventory falls below this threshold number.  
User Activity Lookback | The number of days to look back when assessing whether the customer showed interest in the product.  
Minimum View Time | The number of seconds a user must spend viewing the product with low inventory. Fewer seconds make more products eligible to activate the trigger.  
Sort Items by (descending) | How to sort multiple products with low inventory that meet the view-time requirement. If you configure the campaign to show a limited number of low-inventory items, only the top products based on the sort order are included.  
Catalog Filters | Add filters for product average rating, price, features, or a custom field.  
Behavior Filters | Add filters for user behavior such as whether the user did or didn’t favorite, add to cart, purchase, receive recommendations, or view certain products.  
Triggered Item Frequency Limits | Override the trigger item frequency limit. If you select this option, Personalization ignores the limit in Catalog and Profile Objects.  
Campaign Frequency Limits | Control how many times a triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

