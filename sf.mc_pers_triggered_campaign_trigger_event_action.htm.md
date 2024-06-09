

# Event Action Trigger

Use the Event Action trigger if you want to trigger a campaign based on an
action instead of using a segment. This trigger activates immediately when a
qualified user completes any of the actions you define.

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

![cb484cf5-4ea5-465e-b543-b24628627517]

Tip The Event Action trigger is similar to the Segment Join trigger. If you
want to include multiple achievement criteria, build a segment and use the
Segment Join trigger. For more information, see [Segment Membership
Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_segment_membership.htm&language=en_US&type=5
"A segment membership trigger activates when a user joins or leaves a segment
that you select. Marketing Cloud Personalization updates the segments in real
time, so you can use the triggers to immediately respond to specific user
actions. If you select multiple segments, the user must join or leave only one
of the segments to qualify for the campaign.")

## Setup Requirements

To configure an Event Action trigger, you select from mapped actions in your
dataset and then add campaign frequency limits. If the action you want to use
isn’t mapped, work with your developer to add tracking for that action.

If you add a delay to your campaign and more than one trigger event occurs
during the delay period, the campaign processes the most recent event in the
delay period.

## Configuration Options

When you add this trigger to a triggered campaign, you can set the following
options.

Option | Description  
---|---  
User did any of the specified actions | Specify the mapped user actions to trigger the campaign.  
Campaign Frequency Limits | Control how many times a triggered campaign activates for a profile.  
  
#### See Also

  * [Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5 "Use a triggered campaign to launch a journey when a specific action or event occurs. For example, send a promotion to a shopper who spent time viewing a product but didn’t purchase. You can recommend unread articles or products to a visitor who has spent more than 5 minutes reading about a topic. You can remind new users to complete onboarding steps, or alert sales reps when target prospects spend a certain amount of time on your site. When creating a triggered campaign, you can define when to trigger the campaign, which users to target, and which experiences to deliver.")
  * [Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5 "Frequency limits apply to the number of triggers that Marketing Cloud Personalization sends for a user profile for a specified time period.")

