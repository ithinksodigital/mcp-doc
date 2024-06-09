

# Product Back in Stock Trigger

Use this trigger to reach customers when an out-of-stock product that they
viewed becomes available. The user must have viewed the product while it was
out of stock for a minimum amount of time within a specified number of days.
The trigger checks for products that are back in stock every hour.

You can select this trigger type when you create a campaign. For more
information, see [Create a Triggered
Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5
"Use a triggered campaign to launch a journey when a specific action or event
occurs. For example, send a promotion to a shopper who spent time viewing a
product but didn’t purchase. You can recommend unread articles or products to
a visitor who has spent more than 5 minutes reading about a topic. You can
remind new users to complete onboarding steps, or alert sales reps when target
prospects spend a certain amount of time on your site. When creating a
triggered campaign, you can define when to trigger the campaign, which users
to target, and which experiences to deliver.").

## Setup Requirements

To use this trigger, you must have a numeric product inventory attribute in
your Personalization catalog. Don’t simplify all "in-stock" values to 1.
Rather, use the correct stock amount. When a product is in stock, the value
should always be positive and generally greater than 1. Personalization needs
accurate inventory numbers to determine whether a product is above or below
the out-of-stock threshold.

## Campaign Qualification

For a product to qualify, it must have an inventory greater than 0 for at
least 2 hours and an inventory of 0 for at least 1 week before being back in
stock. You can adjust these thresholds at the dataset level.

If a user completes the ViewItemOutOfStock item action during the user
activity lookback period and hasn’t purchased or back-ordered the product,
Personalization activates the trigger. After the trigger activates,
Personalization checks the campaign rules and configurations to determine
whether to launch the campaign.

## Dataset-Level Configuration Options

The dataset-level configuration is applied to all campaigns that use this
trigger. For example, if you have two Product Back in Stock campaigns, you can
configure different trigger behaviors at the campaign level, but the dataset
configuration applies to both.

Set dataset-level trigger options in Settings > Catalog and Profile Objects >
Catalog Settings > Trigger Items.

Option | Description  
---|---  
Minimum Time Product Out of Stock | The minimum number of days that the product is out of stock before the trigger is activated.  
Minimum Time Product Back in Stock | The minimum number of hours that the product is back in stock before the trigger is activated.  
  
## Campaign-Level Configuration Options

You can set these options when you add a product back in stock trigger to a
campaign.

Option | Description  
---|---  
User Activity Lookback | Set the number of days to look back when assessing whether the customer showed strong intent toward the out-of-stock product. Consider the typical restock schedule for the majority of your product catalog compared to the typical visit frequency of your customers.  
Minimum View Time | Set the number of seconds that a user must spend viewing the out-of-stock product. Fewer seconds make more products eligible to activate the trigger.  
Sort Items by (descending) | How to sort multiple back-in-stock products that meet the view-time requirement. If you configure the campaign to show a limited number of back-in-stock items, only the top products based on the sort order are included.  
Catalog Filters | Add filters for product average rating, price, features, or a custom field.  
Behavior Filters | Add filters for user behavior such as whether the user did or didn’t favorite, add to cart, purchase, receive recommendations, or view certain products.  
Triggered Item Frequency Limits | Override the trigger item frequency limit.   
Campaign Frequency Limits | Control how many times a triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

