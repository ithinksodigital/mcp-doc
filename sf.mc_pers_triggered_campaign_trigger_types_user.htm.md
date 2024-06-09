

# User Triggers

A user trigger activates a campaign based on user behavior.

  * **[Segment Membership Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_segment_membership.htm&language=en_US&type=5)**  
A segment membership trigger activates when a user joins or leaves a segment
that you select. Marketing Cloud Personalization updates the segments in real
time, so you can use the triggers to immediately respond to specific user
actions. If you select multiple segments, the user must join or leave only one
of the segments to qualify for the campaign.

  * **[Cart Abandonment Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_cart_abandonment.htm&language=en_US&type=5)**  
Use the Cart Abandonment trigger to reengage a customer who leaves items in
their cart. When a customer has at least one item in their cart, ends their
visit, and is inactive for 30 minutes, they’re eligible for a Cart Abandonment
trigger. This trigger activates when a user adds an item to their cart but
doesn’t complete the purchase in the same web session. This trigger activates
only one time for a cart, unless the user changes the cart contents. It
activates again if the customer adds items, removes items, or updates item
quantities in the cart.

  * **[Browse Abandonment Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_browse_abandonment.htm&language=en_US&type=5)**  
Use the Browse Abandonment trigger to reengage a customer who spent time
viewing a product but didn’t complete a purchase. A Browse Abandonment
campaign activates when the customer ends their visit, is inactive for 30
minutes, and satisfies trigger rules you set. (If you upload event data for
the user through the Event API, the user is considered active during that
event.)

  * **[Event Action Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_event_action.htm&language=en_US&type=5)**  
Use the Event Action trigger if you want to trigger a campaign based on an
action instead of using a segment. This trigger activates immediately when a
qualified user completes any of the actions you define.

