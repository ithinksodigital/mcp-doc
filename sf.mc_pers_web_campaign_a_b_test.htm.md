

# A/B Test Campaigns

When creating an A/B test campaign, you include multiple experiences, and
assign each experience a percentage of traffic. A/B tests give you flexibility
and control over how Personalization distributes traffic and which users see
which experiences.

## What Is A/B Testing?

A/B testing, in its true definition, is a form of statistical hypothesis
testing with two variants: test and control. An A/B test campaign splits
traffic randomly into different groups and shows each group a variation of a
message.

In Marketing Cloud Personalization, A/B testing more broadly defines a
campaign that uses a randomized split in traffic to test a hypothesis. When
creating A/B test campaigns, you add multiple experiences, and then assign
each a percentage of visitor traffic. The control is a group of people who
qualify to see a campaign but aren’t shown it. The control group creates a
benchmark to measure the success or impact of your campaign. Because users in
this group won’t see the campaign, you can compare the results against the
group that does see the campaign. User behavior, actions, inactions,
affinities, or attributes do not affect A/B tests.

As a best practice for an unbiased, statistically sound test, create messages
as variations of each other. For example, testing a popup message against an
inline message isn’t a true measure of effectiveness because each format
invokes different user behaviors. Therefore, the experiences aren’t
comparable. A better example of an A/B test is a campaign that tests two exit
popup discount codes to determine which is more effective.

## Test Planning

When planning an A/B test, clearly state your testing goals as a hypothesis. A
typical Personalization hypothesis is: "If I change (A) for group (B) of
users, I expect to see (C) results."

Also, research your hypothesis. Before developing your campaign, conduct some
initial analysis to validate that your hypothesis is worth testing. For
example, ask, "Does my hypothesis have a target audience? If so, what’s the
size of that audience? Can I create an audience segment in Personalization?"
The answers to these questions help you to determine the reach of your
hypothesis and resulting campaign.

## Sample Sizes

Data rate and the size of the effect you're looking for helps you determine
how long to run a test. When planning your test, consider using a sample size
calculator to compute the sample size and then run the test. Many sample size
calculators are available online for you to reference. A calculator gives you
an idea of how much data you need for a test, which helps you determine how
long to run the campaign.

In classical statistics, you calculate in advance, and check your result one
time (and only one time) when you have the required data. At that time, you
declare whether any difference you see is real or due to chance. Sample size
calculation is known as a power analysis and is a required step in classical
statistical testing. Because Personalization uses a Bayesian approach, rather
than a classical framework, calculating your sample size isn’t a requirement.
However, doing so can help you with planning if you're unsure about how long
to run a test.

Keep the following in mind if you decide to use a sample size.

  * If you use a sample-size calculator and reach the sample size but don’t reach 95% confidence, you can stop the test and declare no difference. (Or, you can use a difference confidence.) If you reach 95% confidence, you can declare a winner.

  * You can reach confidence sooner than you expect. In contrast to classical testing, Personalization models the underlying distributions directly and typically requires fewer samples. So, if you’re running your test for a month, but see confidence at three weeks, you can stop and declare a difference.

For more information, see [Confidence Explained in Campaign
Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics_confidence.htm&language=en_US&type=5
"Confidence on the Campaign Statistics screen refers to the term statistical
confidence. It’s a measure of how sure you are of your results from an A/B
test. It isn’t a measure of how effective a campaign was, but a measure of how
certain you can be with the campaign’s displayed impact.").

## Adequate Test Time

Follow these recommendations regarding testing time.

  * Resist a rush to judgment. In the early days of the test, it’s best to ignore the campaign statistics because they can change before stabilizing, especially with low-traffic tests.

  * Use multiples of a full week of data. Because user behavior varies across days, a best practice is to include multiples of a full week of data to determine the test winner over time. You can set the beginning and end dates for a web campaign.

  * Allow traffic allocation to adjust. Each user profile is randomly selected for a percentile group. The traffic split doesn’t always reflect experience allocations when you first publish the campaign. As traffic levels increase, the percentages adjust accordingly.

## How Users Are Allocated to Different Test Groups

To determine the experience a user sees, Personalization combines the user’s
user ID and the campaign ID and performs some behind-the-scenes calculations.
When a user sees their experience, statistics are collected that include the
campaign state and data about whether the user was part of the test or control
group. The user continues to see the same experience unless a change to their
profile affects which group they qualify for.

If you don’t see expected impression percentages for your test groups, the
most likely cause is an issue in the experience that prevents one experience
from showing versus another. For example, an experience references an
attribute that some users don’t have, and there’s no default value. Or, an
experience has rules that aren’t satisfied. Or, an experience uses
recommendations that produce no results.

## Test Results

When examining test results, consider that post-test lift can be higher or
lower. Sometimes, even if you have a definite winning test, you can’t
replicate the exact lift you saw in the experiment. The key is that the metric
of the winning test is higher than the other test.

When you do see a winner, a best practice is to check whether you see the same
effect across groups of first-time and returning users. If you don't see the
effect for first-time users, this lift can be due to novelty or "shiny object
syndrome." Your regular users are curious about the change but eventually
revert to their previous behavior. If you do see the effect for first-time
users, it’s more likely to be lasting.

## A/B Testing Across Multiple Campaigns

There are use cases that require targeting multiple content zones with
campaigns to personalize the experience. It’s important to coordinate those
multiple levels of personalization to provide a positive experience for the
user.

For example, you can personalize a homepage hero banner based on a user's
favorite category and show a recommendations zone lower on the page with
recommendations in that same category. To ensure users receive an aligned
experience across both campaigns, you can use A/B test segments to randomize
your audience within a rule-based campaign. Then, you persist that randomized
selection for any experience targeted to the A/B test segment.

#### See Also

  * [Create A/B Test Segments](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_a_b_test.htm&language=en_US&type=5 "Use A/B test segments for tasks like wanting to ensure a user falls into a specific segment across multiple campaigns, or to split campaign traffic into intervals, such as halves, thirds, or quarters.")
  * [Campaign Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics.htm&language=en_US&type=5 "Use Campaign Statistics to measure the impact of your campaigns. The information available on the Campaign Statistics screen helps you analyze where you can make campaign changes to improve results.")
  * [Confidence Explained in Campaign Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics_confidence.htm&language=en_US&type=5 "Confidence on the Campaign Statistics screen refers to the term statistical confidence. It’s a measure of how sure you are of your results from an A/B test. It isn’t a measure of how effective a campaign was, but a measure of how certain you can be with the campaign’s displayed impact.")
  * [Create a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_create.htm&language=en_US&type=5 "Using a web campaign, you can personalize various aspects of your website for your users based on their behavior, affinities, preferences, location, or other qualifying criteria. You can create web campaigns from templates in your dataset. The templates provide a framework that defines the campaign placement, copy and creative locations, and general campaign design.")
  * [ _Video_ : Create A/B Test and Control Groups](https://www.youtube.com/watch?v=-hKk5LufJ0E)

