

# Cart Abandonment Trigger

Use the Cart Abandonment trigger to reengage a customer who leaves items in
their cart. When a customer has at least one item in their cart, ends their
visit, and is inactive for 30 minutes, they’re eligible for a Cart Abandonment
trigger. This trigger activates when a user adds an item to their cart but
doesn’t complete the purchase in the same web session. This trigger activates
only one time for a cart, unless the user changes the cart contents. It
activates again if the customer adds items, removes items, or updates item
quantities in the cart.

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

## Setup Requirements

You must have the AddToCart item action mapped anywhere a user can add an
item, including from quick view windows or from a recommendations block on the
checkout page. Optionally, you can map the item actions ViewCart,
UpdateLineItem, and RemoveFromCart. Work with your developer to capture all
cart-related item actions. For more information, see [Developer Documentation:
Item
Actions](https://developer.salesforce.com/docs/marketing/personalization/guide/item-
actions.html).

Personalization sorts items based on how long the user viewed each item, with
the items they viewed most appearing first. If viewing data isn’t available,
Personalization sorts the items randomly.

## Campaign Qualification and Eligibility

Personalization checks for cart abandonment every 15 minutes. The user must
have updated their cart after at least 30 minutes and after no more than 3
days. If a user abandons a cart, and you create a triggered campaign after
cart abandonment, the triggered campaign can activate for the customer up to 3
days after cart abandonment. If a user completes a purchase, which empties the
cart, the user no longer qualifies for the campaign.

Before sending the message, Personalization evaluates each Cart Abandonment
trigger to make sure it’s still relevant. This check includes whether the user
has purchased abandoned cart items or whether the user has removed all
abandoned cart items. Personalization also checks for any campaign rules you
set, such as segment membership or user behavior filters.

If you add a delay to the campaign, Personalization completes eligibility
checks at the time of the trigger and again after the delay is over.
Personalization adds a 30-minute inactivity check to any delay configured for
the cart abandonment campaign. The campaign doesn’t launch until after the
inactivity check. If more than one cart trigger event occurs during the delay
period, the campaign processes the most recent event in the delay period.

## Configuration Options

When you add this trigger to a triggered campaign, you can set the following
options.

Option | Description  
---|---  
Catalog Filters | Add filters for product average rating, price, features, or a custom field.  
Behavior Filters | Add filters for user behavior such as whether the user did or didn’t favorite, add to cart, purchase, receive recommendations, or view certain products.  
Triggered Item Frequency Limits | Override the trigger item frequency limit. Personalization ignores the limit set in Catalog and Profile Objects.  
Campaign Frequency Limits | Control how many times the triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5 "You can apply user behavior or catalog filters for some triggered campaigns to refine qualification for trigger activation. A user behavior filter is based on customer interaction with the trigger items. A catalog filter is based on catalog attributes. For example, you can add a catalog filter to a product back in stock trigger to have it activate only if the item price is less than $100. Or, you can add a behavior filter so the trigger only activates if the user favorites the product.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

