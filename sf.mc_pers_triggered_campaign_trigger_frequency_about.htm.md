

# About Trigger Frequency

You can set a limit on the number of triggers that Marketing Cloud
Personalization sends for a user profile at a few levels.

## Frequency Limit Configuration

You can set trigger frequency limits when you [create a
campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_frequency_limit.htm&language=en_US&type=5
"When you create a triggered campaign, you configure how many times the
campaign activates for a profile during a specific time or for all time. You
can change the frequency limits for an existing campaign.") or at the
[global](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_global_frequency_limit.htm&language=en_US&type=5
"You can control how many triggers activate during a specific time across all
campaigns and for every item in your catalog. For example, you can set a
global trigger frequency limit to 3 times a week, 12 times a year, and 50
times maximum. This limit applies to all campaigns and items.") and [trigger
item](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_item_frequency_filter.htm&language=en_US&type=5
"Set how often a trigger item appears during a campaign at the item level.")
levels.

## Limit Evaluation

Personalization evaluates all frequency limits when the trigger occurs and
again after any delay you configure for a campaign. Imagine you have a global
or campaign frequency limit of no more than one per day and three per week.
User or catalog behavior triggers the campaign every day. After the third day,
Personalization blocks the campaign because it has reached the frequency limit
of three per week. If there’s a conflict between frequency limits, the lowest
frequency wins. Personalization evaluates the global setting first, and then
the campaign level setting. Therefore, if the global setting is lower than the
campaign setting, Personalization blocks the campaign after it reaches the
global limit.

