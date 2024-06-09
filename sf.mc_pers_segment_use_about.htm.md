

# About Using Segments

Learn about using segments.

## Ways to Use Segments in Campaigns

There are several ways you can use segments to increase the impact of your
campaigns:

Approach | Description  
---|---  
Personalize campaigns | You can target segments of users with specific personalized content. For example, you can show first-time users an introductory video about your company, but not show it the next time they visit your site.  
Set goals and filters | You can use a segment to specify certain actions as the goals for a campaign. For example, the goal for first-time users who watch your introductory video is to connect with an advisor by completing a short web form. You can also use segments to set a global goal.   
Filter statistics | You can use segments to filter campaign statistics to see how various groups of users are reacting to a campaign.  
Analyze trends and engagement | You can see trends in a particular segment, view specific users or accounts in a segment, or compare data across multiple segments. With Segment Compare, you can compare certain segments with other segments, or with your entire site, to see differences in key metrics and behaviors. You can also filter reports by segments to learn more about a segment's behavior.  
Analyze member details | Each segment user has a [Unified Customer Profile](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_customer_profile.htm&language=en_US&type=5 "The Unified Customer Profile provides a comprehensive view of each of your users—visitors, customers, prospects, and subscribers—based on their interactions with your various channels.") that shows specific details about their behavioral data.  
Import or export segment membership | You can sort and export segment data, including any defined segment rules. You can also synchronize segments with your CRM so you can include everything the Personalization system captures about a lead, contact, or account.  
  
## Campaign Qualification

You can use segments to show a campaign to a specific subset of users based on
the criteria you set. For example, you only want to show a campaign to users
who have read three blog articles today. You already have a segment that
captures users who meet this criteria, so you can use it to create a campaign-
wide rule.

In this example, users who read their second blog article today don't qualify
to see the campaign. As soon as those users read their third blog, they
immediately join the segment and qualify to see the campaign. See Add Rules
for Campaigns, Experiences, and Messages for more information.

## Experience Qualification

There are several ways to determine the effectiveness of campaign experiences
against each other and against a control group:

How Determine | Description  
---|---  
A/B testing | Split traffic randomly into different groups and show each group variations of a message to see which version is most effective.  
Rule-based testing | Create multiple experiences, then assign rules that control the visibility of each experience to target specific groups of visitors.  
  
## Retail Examples

The following examples show ways to use segments for retail business.

Target | Strategy | Settings  
---|---|---  
Cart abandonment | Prevent cart abandonment with a bounce message campaign. | Category: ItemsRule: Item Action CountRule parameters: added to cart, any, Products, at least, 1, todayANDCategory: ItemsRule: Item Action CountRule parameters: purchased, any, Products, at most, 0, today  
Upsell | Group users who purchase a certain value in a specified time period, so you can target them with a campaign for an upsell. | Category: ItemsRule: Purchases ValueRule parameters: Purchased between, $XX, and $XXX, worth of any, Products, in the last, X days  
Lifetime Value | Group your high-value customers so you can target them or analyze their behavior. | Category: ItemsRule: Purchases ValueRule parameters: Purchased at least, $XXXX, worth of any, Products, in the last, X days  
Persona | Identify your customers by their affinities for brand, category, price, and so forth, and create personalized campaigns for them. | Category: ItemsRule: FavoriteRule parameters: Select an option from the **User’s favorite** dropdown and configure the applicable parameters.  
Lead generation | Identify users who haven’t signed up for your email marketing efforts. | Category: ThirdpartyRule: External IDRule parameters: has or does not have; select the application and configure the applicable parameters.  
Location | Identify your International users. | Category: LocationRule: InRule parameters: User’s country, is not one of, United States  
  
## Travel Examples

The following examples show ways to use segments for travel business.

Target | Strategy | Settings  
---|---|---  
Persona | Identify users based on actions they take on your site. | Category: ActionsRule: Action CountRule parameters: User did, any of specific actions, enter an action and configure its settings   
Location | Identify users based on location | Category: LocationRule: InRule parameters: User’s country, is one of, select country  
Lead generation | Group users that subscribe to your other marketing channels, so that you can communicate with them in a more personalized manner. | Category: MetricsRule: Text AttributeRule parameters: User Name (userName), existsANDCategory: MetricsRule: Text AttributeRule parameters: External User ID (extUserId), exists  
Upsell | Identify users that purchased during a previous season and deliver a targeted upsell. | Category: ItemsRule: Purchases ValueRule parameters: Purchased at least, $1, worth of any, Products, between dates, MM/DD/YYYY and MM/DD/YYYY  
Behavior | Group users based on the content they interact with, such as users who look at wedding-related content. | Category: ItemsRule: Item Action CountRule parameters: viewed, specific, Category, enter a category, at least, 1 times, for all time  
  
## Customer Success

The following examples show ways to use segments to target customer success.

Target | Strategy | Settings  
---|---|---  
First login | Identify users that log in for the first time. | Category: VisitsRule: Time Since FirstRule parameters: Visited, for the first time for all timeANDCategory: VisitsRule: AnonymousRule parameters: User is not anonymous  
No login | Identify users that don’t log in for a certain amount of time. | Category: VisitsRule: Visit RecencyRule parameters: Did not visit, in the last X days  
New feature usage | Identify users that use a new feature. | Category: ActionsRule: Action CountRule parameters: User did, any of specific actions, enter an action, at least 1 time, for all time  
Feature usage | Identify users that use one feature, but not another. | Category: ActionsRule: Action CountRule parameters: User did not do, any of specific actions, enter an action, at least 1 time, for all timeANDCategory: VisitsRule: Time Since First VisitRule parameters: Visited, for the first time in the last, 15 daysANDCategory: ActionsRule: Action CountRule parameters: User did, any of specific actions, enter an action, at least X times, for all time  
Subscription change | Identify users that have a change in their subscription level. | Category: SubscriptionRule: Time Since LifecycleRule parameters: transitioned from Customer (Pick), to Customer (Paying), in the last, 30 days and, stayed in that state  
Unsubscribed | Identify users that unsubscribe from email or push notifications. | Category: MetricsRule: Text AttributeRule parameters: Exact Target Status (etStatus), equals, unsubscribed  
  
## Demand Generation

The following examples show ways to use segments for demand generation.

Target | Strategy | Settings  
---|---|---  
Engaging with blogs | Identify users who read your blogs. | Category: ActionsRule: Action CountRule parameters: User did, any of specific actions, enter an action (such as Blog - View Article), at least X times, for all time  
Engaging with email | Identify users who sign up for email. | Category: MetricsRule: Text AttributeRule parameters: Email Address (emailAddress), exists  
Engaging with content but not video | Identify users who view content, but not video. | Category: ItemsRule: Action CountRule parameters: Viewed, any, Products, at least, 1 times, for all timeANDCategory: ActionsRule: Action CountRule parameters: User did not do, any of specific actions, enter a video option, at least X times, for all time  
Engaging with favorite products | Identify users by a favorite product. | Category: ItemsRule: FavoriteRule parameters: User’s favorite Category, enter a category, measured by viewed, for all time  
Engaging with demos | Identify users from a known company that request a free demo. | Category: ActionsRule: Action CountRule parameters: User did, any of specific actions, enter a demo action, at least 1time, for all timeANDCategory: LocationRule: CompanyRule parameters: User’s Company is known  
Engaging with free trials | Identify users that participate in a free trial and log in multiple times. | Category: MetricsRule: Text AttributeRule parameters: UserAccountType, equals, Free TrialANDCategory: VisitsRule: Visit CountRule parameters: Visited, 1 or more times, for all time  
Engaging with customers | Identify users who log in. | Category: ActionsRule: Action CountRule parameters: User did, any of specific actions, ClickedLogin, at least 1 time, for all time

