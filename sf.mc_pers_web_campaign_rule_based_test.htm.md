

# Campaign Targeting Rules and Rule-based Tests

Rules determine when, where, and how your campaigns display and who sees them.
You can add rules when you create or edit a campaign at the campaign level for
campaign targeting or when defining rule-based test experiences.

## Campaign Targeting Rules

Set rules at the campaign level when you want to control how a web campaign
displays. Control visibility at the campaign-level based on segments,
location, device type, time of day, viewer actions, page, company, industry,
and more.

Campaign targeting rules follow AND logic. If you include multiple rules in
the same web campaign, users must satisfy all rules, regardless of the order,
to qualify for the campaign.

You can use campaign targeting rules for rule-based test campaigns and A/B
test campaigns. In a rule-based test campaign, users must qualify at the
campaign level first and then qualify for a specific experience. In an A/B
test campaign, users must qualify for the campaign first. Then they either see
the campaign or become part of the control group, which doesn’t see the
campaign.

## Rule-based Test Campaigns and Experience Rules

Deliver specific experiences to specific groups or segments of people based on
who they are or where they are in your site or app. A simple way to think
about rule-based testing is with IF-THEN statements. IF a person falls into
segment A, THEN show them experience A. IF a person falls into segment B, THEN
show them experience B, and so on.

In a rule-based test campaign, users must qualify to receive the campaign
experience and each experience needs a qualifying rule. Experience rules are
available for rule-based test campaigns only. Users qualify for an experience
based on page target or type, user location, user segment, visit behavior,
event action, and more.

Users who qualify for multiple experiences within the campaign receive the
experience at the top of the list of rule-based experiences. You can reorder
the experiences to fit your business needs.

If you set a control percentage, it applies only to users who qualify for the
experience. The control is a group of people who qualify to see a campaign but
aren’t shown it. The control group creates a benchmark to measure the success
or impact of your campaign. Because users in this group won’t see the
campaign, you can compare results against the group that does see the
campaign.

## Example Scenario

Suppose you have a campaign with device-specific messages that you want to display only to returning users from your six target cities. At the campaign-targeting level, a **Visit Behavior** | **Visit Count** rule determines whether the user sees the campaign based on a previous visit to your website. Then, using a rule-based test campaign with experience-level rules, you can filter who sees which location and a device-specific experience based on user location and device type.

#### See Also

  * [ _Video_ : Create Rule-Based Campaigns](https://www.youtube.com/watch?v=7frznbLswhk)
  * [Rule Categories](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_rule.htm&language=en_US&type=5 "There are a variety of rules that you can add for campaign targeting and rule-based campaign experiences when you create or edit a campaign.")
  * [Create a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_create.htm&language=en_US&type=5 "Using a web campaign, you can personalize various aspects of your website for your users based on their behavior, affinities, preferences, location, or other qualifying criteria. You can create web campaigns from templates in your dataset. The templates provide a framework that defines the campaign placement, copy and creative locations, and general campaign design.")

