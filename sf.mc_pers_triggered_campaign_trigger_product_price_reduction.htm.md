

# Product Price Reduction Trigger

Use this trigger to reach customers when a product they viewed but didn’t
purchase drops in price. The user must have viewed the in-stock product for a
minimum amount of time within a specified number of days. Marketing Cloud
Personalization uses a minimum view time to filter out customers that look at
a product only for 1 second before they navigate away. The trigger checks
every 30 minutes for qualifying products that have a price drop greater than
the configured minimum price percent reduction.

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

## Campaign Qualification

For a product to qualify, it must have the same price for at least 1 week
before the reduction. The reduced price must remain unchanged for at least 2
hours for Personalization to update it in your catalog and trigger the
campaign. You can adjust these thresholds at the dataset level.

## Dataset-Level Configuration Options

The dataset-level configuration is applied to all campaigns that use this
trigger. For example, if you have two Price Reduction campaigns, you can
configure different trigger behaviors at the campaign level, but the dataset
configuration applies to both.

Configure dataset-level trigger options in Settings > Catalog and Profile
Objects > Catalog Settings > Trigger Items.

Option | Description  
---|---  
Minimum Time for Reduced Price  | The minimum number of hours that the new price is available for a product before the trigger is activated.  
Minimum Time for Original Price | The minimum number of days that the product had the previous price before the trigger is activated.  
  
## Campaign-Level Configuration Options

You can set these options when you add a price reduction trigger to a
campaign.

Option | Description  
---|---  
Minimum Price Percent Reduction | The minimum percentage between 5–100 that the product price must drop. Determine the percentage based on what you typically mark down the majority of your product catalog during a sale.  
User Activity Lookback | The number of days to look back when assessing whether the customer showed strong intent toward the product with the price drop. Consider the typical frequency of price changes in your product catalog compared to the typical visit frequency of your customers.  
Minimum View Time | The number of seconds a user must spend viewing the product. Fewer seconds make more products eligible to activate the trigger.  
Sort Items by (descending) | How to sort multiple products with a price drop that meet the view-time requirement. If you configure the campaign to show a limited number of reduced price items, only the top products based on the sort order are included.  
Catalog Filters | Add filters for product average rating, price, features, or a custom field.  
Behavior Filters | Add filters for user behaviors such as whether the user did or didn’t favorite, add to cart, purchase, receive recommendations, or view certain products.  
Triggered Item Frequency Limits | Override the trigger item frequency limit. If you select this option, Personalization ignores the limit in Catalog and Profile Objects.  
Campaign Frequency Limits | Control how many times a triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

