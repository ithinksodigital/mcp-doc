

# About Mobile Campaign Rules

Learn about mobile campaign rules.

### Required Editions

Available in: Premium Edition  
---  
  
## Rule Types

There are three types of rules that affect when, where, and how your mobile
campaigns display and who sees them.

  * [Mobile Campaign-Wide Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_global_rules.htm&language=en_US&type=5 "For all types of mobile campaigns, campaign-wide rules control visibility at the campaign level based on things such as segments, visit count, visit duration, user actions, and date and time. Set rules at the campaign level when you want to holistically control how a campaign displays for qualified mobile app users.") control visibility at the campaign level based on things such as segments, visit count and duration, and user actions. Set rules at the campaign level when you want to holistically control how and when mobile app users see a campaign. With campaign-wide rules, qualification happens at the campaign level so users must meet the rules you set to see any part of the campaign.

  * [Mobile Experience-Level Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_experience_level_rules.htm&language=en_US&type=5 "For all types of mobile campaigns, if you set experience-level rules, each experience needs a qualifying rule. Mobile app users who qualify for the campaign see the first experience in the list for which they qualify. If you set a control percentage, it applies only to users who have qualified for the experience.") are available only for rule-based campaigns. They control qualification criteria of campaign experiences based on segments and actions. When you create a campaign, it’s automatically in A/B test mode, so each experience you create in the campaign displays to qualified mobile app users at random. When you change the test mode to rule-based, you can add an experience-level rule to each experience to control which users see which experience. 

  * [Mobile Message-Level Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_message_level_rules.htm&language=en_US&type=5 "Message-level rules control visibility at the message level based on mobile app user actions and display frequency. For Mobile In-App Message and Mobile Push campaigns, you can use the message level to define who sees your message and when.") control visibility at the message level based on user actions and display frequency.

## Campaign Visit Count

A campaign-level Visit Count rule determines whether the user sees the
campaign based on a previous visit to your mobile app.

## Target Users from Different Cities

Create a campaign with different experiences for segments of mobile app users
from different cities. You can then define a Target Users rule to match the
users with the experience intended for them.

## Target Users Who Add to the Cart

Use a Target Pages message-level rule to remind mobile app users who have
items in the cart that they get free shipping when they spend a certain
amount.

