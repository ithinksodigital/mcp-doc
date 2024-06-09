

# Segment Categories and Rules

Marketing Cloud Personalization provides various categories and accompanying
rules for use with segments. When a user interacts with one of your channels,
the Personalization system identifies the segments they belong to based on
real-time session activity. Because segment updates happen in real time,
membership changes occur immediately.

## Campaigns

Using this category, you can create segments based on a user’s engagement with
your campaigns.

Rule | Description  
---|---  
Campaign Stat Count | Whether the user views, clicks, dismisses, or qualifies to view (based on control group membership) the selected campaign, any experience, or a specific experience for the specified number of times.  
A/B Test Segment | Randomly sorts users into as many segments as desired across your entire user base, totaling 100%. For example:

  * Segment A: 0%–15%
  * Segment B: 15%–30%
  * Segment C: 30%–50%
  * Segment D: 50%–85%
  * Segment E: 85%–100%

This rule isn’t inclusive, so the ending percentage of one segment must be the
beginning percentage of the next segment. You can use this rule to randomly
generate groups of users for analytics, or to ensure that users see a
consistent test or control experience across multiple campaigns.  
Campaign Stat Recency | Whether the user views, clicks, dismisses, or qualifies to view (based on control group membership) the selected campaign, any experience, or a specific experience during the past specified number of days.  
  
## Actions

With the Actions category, you can create segments based on whether a user performs a specific action or group of actions, the frequency, and recency of those actions. Actions vary by dataset. You can view the actions for your dataset by selecting **Reports** | **Actions**.

Rule | Description  
---|---  
Action Count | Whether the user performs any action, or any or all of specific actions a specified number of times during a defined time period  
Time Since First Action | Whether the user performs a specific action for the first time during a defined time period  
Action Recency | Whether the user performs any action, or any or all of specific actions during the past specified number of days  
Page View Count | Whether the user views a specific number of pages during a defined time period  
  
## Subscription

Using this category, you can create segments based on a subscription level or
where a user or account is in the lifecycle of a subscription. The location of
this segment rule option is dependent on your dataset configuration. For B2C
sites, the Personalization system tracks it at the user level. For B2B sites,
the Personalization system typically tracks the subscription at the account
level.

![7b45e40a-5b11-4330-9573-c73f0264b197]

Note This category is available to customers with Account Profiles sites only.

Rule | Description  
---|---  
Lifecycle State | Whether the user is at the specified subscription level  
Time Since Lifecycle Transition | Whether the user transitions from the specified subscription level to another specified subscription level during a defined time period, and stays in that state  
  
## Visits

Using this category, you can create segments based on a user’s visit data.

Rule | Description  
---|---  
Visit Count | Whether the user visits a specified number of times during a defined time period  
Anonymous User | Whether the user is anonymous  
Originating Referrer | Whether the user's originating referrer URL, medium, source name, search terms, domain, or subdomain meets the specified criteriaFor medium, Marketing Cloud Personalization identifies the medium by parsing the URL of the originating referrer and comparing its domain, and any available parameters, to identified medium providers. When Personalization finds a match, it’s categorized into one of the supported mediums. See [Originating Referrer Domain to Medium Mapping](https://salesforce.quip.com/3vIeAPsKV5YE) for a list of originating referrer domains categorized to their respective medium.  
Time Since First Visit | Whether the user visits for the first time during a defined time period  
Visit Source | Whether the user visits from a mobile device or from the web at least one time during a defined time period This option is available only if there’s a mobile app connected to the Personalization system.  
Visit Recency | Whether the user visits within the past specified number of days  
Visit Duration | Whether the user visits for more than a specified number of seconds, minutes, or hours during a defined time period  
  
## Location

Using this category, you can create segments based on a user’s location.

Rule | Description  
---|---  
In | Whether the user's ZIP code (US only), city, metro, state/region, or country is known or part of the defined list  
Company | Whether the user's company is known, is equal to, or contains one or more specified organization names. Start typing to see options. This rule is available only if you have B2B Detect  
ISP | Whether the user's ISP is known or contains one of the specified ISP names  
Near | Whether the user's ZIP code (US only), city, or latitude-longitude is within a specified number of miles of the specified ZIP code, city, or latitude-longitude  
Industry | Whether the user's industry is known or is one of the specified industries. To see options, start typing. This rule is available only if you have B2B Detect  
  
## Metrics

Using this category, you can create segments for certain metrics based on
information that you provide during your implementation.

Rule | Description  
---|---  
Engagement | Whether the user's engagement score meets the defined criteria and percentage  
Ordered Funnel Status | Whether the selected funnel status is at, before, or after the specified funnel step  
Text Attribute | Whether the selected attribute meets the defined criteria  
KPI | Whether the selected KPI value or percent (%) change for a user meets the defined criteria  
  
## Third Party

This category option is available only if you have a first-class third-party
email provider syncing with the Personalization system.

Rule | Description  
---|---  
External ID | Whether a known Personalization user ID has the defined third-party application ID  
  
## Items

Using this category, you can create segments based on items in your catalog.

Rule | Description  
---|---  
Action First Time | Whether the user completes the specified action for the first time during a defined time period  
Order Value | Whether the user's total or average order value is at least, at most, or between a specified dollar amount during a defined time period  
Order Count | Whether the user's number of orders is at least, at most, or between a specified number during a defined time period  
Order First Time | Whether the user's first order is during a defined time period  
Cart Contents | Whether the shopping cart item count or total value is at least, at most, or between a specified dollar amount  
Purchases Value | Whether the user purchases a specific dollar amount for any category or for specific categories during a defined time period  
Cart Adds Value | Whether the user adds a specific dollar amount to their cart for any category or for specific categories during a defined time period  
Favorite | Whether the user's favorite category is a defined item (name or ID) for the specified criteria during a defined time period  
Time Spent | Whether the user views any category or specific categories for a specific duration of seconds, minutes, or hours during a defined time period  
Action Count | Whether the user completes the specified action at least, at most, or between the specified number of times during a defined time period

