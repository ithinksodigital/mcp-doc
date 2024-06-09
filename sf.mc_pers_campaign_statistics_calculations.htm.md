

# Campaign Statistics Calculations

Campaign statistics are available for every Personalization campaign. The
calculations and information available on the campaign statistics screen helps
you determine the success of your campaign.

## Lift is the Objective

The objective for any A/B test or personalization campaign is to generate lift
over control for a business goal. The impact of the campaign is the
measurement of the generated lift.

  * Lift is a statistically significant improvement in a measured business goal.

  * Control is the default experience without the change included or personalization applied.

  * The business goal is what you use to define campaign success. It must include something you can measure. For example, you can measure a click-through, a sign-up, the amount of time on a page or site, a purchase, average order value, and revenue per user. A business goal includes a specific amount of improvement. 

Lift is calculated by looking at the percentage increase of the goal value
after running the campaign. It can be written as a mathematical equation:

[(Goal value for a test experience) – (Goal value for control)] / (Goal value
for control)]

For more details, see the examples section later in this section.

## Goal Completion Criteria

What counts as a goal completion? What counts in the calculations for revenue
per user, click-through, signup, segment membership, and average order value?
Personalization calculates results only as part of the analysis if a visitor
meets these criteria.

  * Qualification—The visitor qualifies to see the campaign and is either in the test group and receives a personalized experience or is in the control group and doesn’t receive a personalized experience.

  * Completion—The visitor achieves the selected goal after qualifying for the campaign. Similarly, Personalization counts attributed revenue per user for visitors who qualify for the campaign and make a purchase. 

  * Time Range—For attribution, Personalization only considers activity inside the time frame that you select. For a purchase to be attributed, the selected campaign interaction, the impression or click, and the goal event must happen within the time frame. Goal events include purchases, clicks, or goal achievements. For more information, see [Attribution Time Frame Explained in Campaign Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics_attribution_time_frame.htm&language=en_US&type=5 "Personalization attributes your visitors’ purchase goal completions based on their interaction, and their level of interaction, with Personalization campaigns.").

## Statistics Granularity

If you see differences between the campaign list screen and the campaign stats
screen for the same period, it's because the statistics are stored
differently. The campaign list screen is designed to load quickly and not
aggregate total impressions, clicks, goal completions, and other data. And it
uses a different counting system to fetch campaign statistics data. The
campaign stats screen loads slower, but presents up-to-the-minute campaign
data. The data from the campaign statistics screen is your source of truth,
despite any differences.

## Confidence

For each metric calculated incrementally, Personalization shows you how much
better a campaign experience performs compared to the selected comparison
baseline. Confidence tells you how sure you can be that the experience drives
the positive or negative result. Personalization considers a result to be
statistically confident if it has a confidence rating of at least 95%. A bold
arrow when you hover over the result indicates that it’s statistically
confident.

When you think about the importance of confidence, keep these considerations
in mind.

  * Don’t draw significant conclusions from small amounts of data. In Example 2 in the Examples section, Experience 1 performs 35% better than the control. But confidence is 0% because only 33 people’s actions contribute to the goal completion rate, which isn’t enough to be statistically significant.

  * The data patterns matter. The patterns in the data can make you more or less sure of the results.

## Bayesian Analysis

Personalization uses [Bayesian
analysis](https://betterexplained.com/articles/an-intuitive-and-short-
explanation-of-bayes-theorem/) to continuously calculate and update the
confidence of every lift percentage.

  * If the Bayesian analysis is greater than 95%, Personalization shows the percentage of confidence and whether the campaign is winning or losing versus the control.

  * If the Bayesian analysis is less than 95%, Personalization still shows the result, but it indicates that the results are inconclusive.

For more information about interpreting campaign statistics data, refer to the
See Also section.

## Lift Calculation: Example 1

Suppose the goal of a personalization campaign is to increase revenue per
user. The control for the campaign is an experience without any
recommendations. When visitors who qualify for the campaign see the control
experience, revenue per user is $77.13. When visitors who qualify for the
campaign see the personalized experience, which shows recommendations targeted
to each visitor’s affinities and preferences, revenue per user is $84.69. The
campaign has a 9.8% lift, which is calculated as:

(84.69 - 77.13) / (77.13) = 9.8%

## Lift Calculation: Example 2

Now consider another campaign set up as an A/B test. The goal of this A/B test
campaign can be anything that you want to improve on your site. Goals include:

  * Increasing clickthroughs
  * Visitors joining a segment of interest
  * Shoppers signing up for emails
  * Visitors spending a certain amount of time on the site 

When visitors qualify for this example campaign and see the control
experience, they achieve the goal at a rate of 1.01%. When visitors qualify
for this example campaign and see the personalized experience, they achieve
the goal at a rate of 1.36%. Lift is calculated by looking at the percentage
increase of the goal value after running the campaign:

[1.36- 1.01] / [1.01] = 34.9%

The personalized experience seems to be generating 34.9% lift, but the
campaign statistics show confidence at 0%. Given inconclusive results, the
34.9% lift can’t be seen as an accurate reflection of success. Why is the
confidence 0% and what does that mean? For more information, see [Confidence
Explained in Campaign
Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics_confidence.htm&language=en_US&type=5
"Confidence on the Campaign Statistics screen refers to the term statistical
confidence. It’s a measure of how sure you are of your results from an A/B
test. It isn’t a measure of how effective a campaign was, but a measure of how
certain you can be with the campaign’s displayed impact.").

## Comparing Personalization Statistics With Reporting Data From Third-Party
Analytics Providers

In addition to using Personalization campaign statistics, organizations often
use third-party analytics software to track campaign effectiveness. In some
cases, Personalization campaign statistics can differ from statistics gathered
by third-party software. Many data points contribute to how Personalization
tracks and records campaign statistics, like configuration, timing, and the
definitions of a user or visit. Reporting for Personalization can differ from
the way analytics providers track the same information, making it difficult to
pinpoint a single reason for a mismatch. For more information about the
Personalization approach to data tracking and reporting, see [Reports and
Analytics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_report_analytics.htm&language=en_US&type=5
"After personalizing your site, use Personalization reports to determine
what’s working and where to make improvements.") and developer documentation
for [Campaign Stats
Tracking](https://developer.salesforce.com/docs/marketing/personalization/guide/campaign-
stats-tracking.html?q=campaign%20stats%20tracking).

