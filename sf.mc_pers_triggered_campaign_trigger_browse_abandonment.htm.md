

# Browse Abandonment Trigger

Use the Browse Abandonment trigger to reengage a customer who spent time
viewing a product but didn’t complete a purchase. A Browse Abandonment
campaign activates when the customer ends their visit, is inactive for 30
minutes, and satisfies trigger rules you set. (If you upload event data for
the user through the Event API, the user is considered active during that
event.)

You can select and configure this trigger type when you create a triggered
campaign. For more information, see [Create a Triggered
Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5
"Use a triggered campaign to launch a journey when a specific action or event
occurs. For example, send a promotion to a shopper who spent time viewing a
product but didn’t purchase. You can recommend unread articles or products to
a visitor who has spent more than 5 minutes reading about a topic. You can
remind new users to complete onboarding steps, or alert sales reps when target
prospects spend a certain amount of time on your site. When creating a
triggered campaign, you can define when to trigger the campaign, which users
to target, and which experiences to deliver.").

## Campaign Qualification and Eligibility

The user must have completed one of the required item actions during their
visit: ViewItem, QuickViewItem, or ViewItemDetail. And, the user must not have
purchased qualifying items in the past two days (or three days, depending on
account timezone).

If a user views multiple items that qualify for the campaign and purchases
some of those items, the user is still eligible for a Browse Abandonment
triggered campaign for the unpurchased items. To avoid this behavior, add a
purchase behavior filter to the campaign. For more information, see [Behavior
Filters](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_behavior_filter.htm&language=en_US&type=5
"A user behavior filter is based on customer interaction with the trigger
items. Your developer configures these item actions in your account. You can
add multiple user behavior filters, and the user must meet all the criteria to
qualify for the trigger.").

Personalization evaluates each Browse Abandonment triggered campaign before
sending to make sure it’s still relevant for the customer. It checks for
browse abandonment every hour and checks to see if the customer has visited
again before showing the campaign.

If you add a delay to the campaign, Personalization completes eligibility
checks at the time of the trigger and again after the delay is over.
Personalization adds a 30-minute inactivity check to any delay set for the
Browse Abandonment campaign. The campaign doesn’t launch until after the
inactivity check. If more than one trigger event occurs during the delay
period, the campaign processes the most recent event in the delay period.

You can add catalog filters and behavior filters that further refine trigger
activation qualification rules. Personalization checks that the user meets any
qualification rules before showing the campaign, including any campaign rules
you set, such as segment membership or filters.

## Configuration Options

When you add this trigger to a triggered campaign, you can set the following
options.

Option | Description  
---|---  
Only Trigger if Cart is Empty | Personalization sends the campaign only if the user's cart is empty. For more information about tracking a customer's cart, see [Cart Abandonment Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_cart_abandonment.htm&language=en_US&type=5 "Use the Cart Abandonment trigger to reengage a customer who leaves items in their cart. When a customer has at least one item in their cart, ends their visit, and is inactive for 30 minutes, they’re eligible for a Cart Abandonment trigger. This trigger activates when a user adds an item to their cart but doesn’t complete the purchase in the same web session. This trigger activates only one time for a cart, unless the user changes the cart contents. It activates again if the customer adds items, removes items, or updates item quantities in the cart.").  
User Viewed Item for at least | Personalization sends the campaign if the user views the item for the minimum time you set. The lower you set this threshold, the more products are eligible to activate the Browse Abandonment trigger. To determine a threshold to set, look at average view times for products on your site.A Browse Abandonment campaign includes all items that meet the browse abandonment minimum threshold you set. For example, imagine a user views five products during their visit but only views three of them for the minimum time you’ve set. The campaign only includes the three products they viewed for the minimum time. You can restrict the number of items you include in the campaign if your developer includes that option in the campaign template.Personalization sorts items based on how long the user viewed each item, with the items they viewed most appearing first. If viewing data isn’t available, Personalization sorts the items randomly.  
Catalog Filters | Add filters for product average rating, price, features, or a custom field.  
Behavior Filters | Add filters for user behavior such as whether the user did or didn’t favorite, add to cart, purchase, receive recommendations, or view certain products.  
Triggered Item Frequency Limits | Override the trigger item frequency limit. Personalization ignores the limit set in Catalog and Profile Objects.  
Campaign Frequency Limits | Control how many times the triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

