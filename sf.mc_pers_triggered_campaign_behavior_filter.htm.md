

# Behavior Filters

A user behavior filter is based on customer interaction with the trigger
items. Your developer configures these item actions in your account. You can
add multiple user behavior filters, and the user must meet all the criteria to
qualify for the trigger.

You can add a user behavior filter when creating certain triggered campaign
types.

Behavior Filter | Description  
---|---  
Favorite | The user did or didn’t favorite the trigger item or any item during the specified number of days. Because Marketing Cloud Personalization doesn’t store a user’s favorite list as an object, the trigger checks only whether the user completed the favorite item action based on how you configure the filter.  
Add to cart | The user did or didn’t add the trigger item or any item to their cart. Because Personalization stores the user’s cart as an object, the filter checks for the trigger items that are in the user’s cart when the trigger occurs and again after any delays that you set for the campaign. The trigger doesn’t activate if the user removes the item from the cart or purchases the item.  
Purchase | The user did or didn’t purchase the trigger item or any item during the specified number of days.  
Get recommendations for | The user did or didn’t get recommendations for the trigger item or any item during the specified number of days.  
View | The user did or didn’t view the trigger item or any item during the specified number of seconds.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")

