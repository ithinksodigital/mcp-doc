

# New Item in High-Engagement Category Trigger

Reach users when you add a catalog item in a category that they’ve expressed
high interest in. This trigger checks for new items in the user’s high-
engagement categories every 6 hours and activates if the user hasn’t viewed
any of the items for the specified minimum view time. A high-engagement
category is based on behavior criteria that you set, such as view time and a
minimum number of items purchased.

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

You can set these options when you add this trigger to a campaign.

Option | Description  
---|---  
Item Type | Specify the type of catalog item. This trigger uses the primary catalog items in Marketing Cloud Personalization: Product, Article, and Blog. It doesn’t use custom catalog objects.   
User Activity Lookback | The number of days to consider when determining whether a user is highly engaged with a category. Base the number of days on the typical visit frequency of your more engaged customers.  
Category Minimum View Time | The number of minutes that a highly engaged user must spend viewing items in the category during the user activity lookback period. Fewer minutes make more categories eligible as high-engagement categories, and the trigger activates for more categories.  
Category Minimum Purchases | The number of purchases the user must make during the activity lookback time period to be considered highly engaged with the category. To limit the number of high-engagement categories, the Category Minimum View Time setting is applied.  
Enable Created Date Fallback | If the item doesn’t have a Published Date attribute, select this option to use the date that the product first appeared in your Personalization catalog. You can populate this value through the site map or through an ETL data feed.   
Catalog Filters | Add filters for product average rating, price, features, or a custom field.  
Behavior Filters | Add filters for user behavior such as whether the user did or didn’t favorite, add to cart, purchase, receive recommendations, or view certain products.  
Triggered Item Frequency Limits | Override the trigger item frequency limit.   
Campaign Frequency Limits | Control how many times a triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

