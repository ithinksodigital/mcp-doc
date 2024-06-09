

# Results Filter Attribution Statistics

How Personalization calculates attribution statistics can depend on whether
individuals are included or excluded from the calculations based on their
campaign activity.

![1c8724b9-df93-47c0-93ca-eb6506664d53]

Attribution statistics (1) show values attributed to individuals who have
completed the campaign goal, such as a conversion or purchase. Whereas
activity statistics (2) include values for all individuals who engaged with
the campaign, regardless of whether a conversion or purchase occurred.

When you select a results filter, Personalization applies the filter against
campaign events (impressions, views or clicks, and conversions or goals) for
the selected start and end dates and time settings. For Personalization to
include individuals in attribution statistics, they must match the selected
filter for all campaign events within the time range. If they don’t meet this
criteria, Personalization excludes the individuals from calculations.

For example, a site visitor impresses anonymously and then logs in to make a
purchase, all within the attribution window time frame. The visitor uses both
user states (Anonymous and Logged In) and makes a purchase within the
attribution window, so Personalization doesn’t include that visitor in
attribution calculations when the Results Filter is set to Anonymous. Because
individuals aren’t included in the filtered calculation under these
conditions, sums of complementary filters, such as Anonymous and Logged In,
don’t always match unfiltered totals.

#### See Also

  * [Campaign Statistics Filters](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics_filters.htm&language=en_US&type=5 "Use campaign statistics filters to focus on how various subgroups behave in a campaign. You can view statistics based on selected results filters, tailor statistics output to account for outliers, view statistics by attribution and activity, or compare baselines.")
  * [Get Statistics for a Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics_view.htm&language=en_US&type=5 "Monitor and analyze the effectiveness of a campaign. You can apply different filters to view activity and attribution metrics during a particular time period. To collect statistics, the campaign must have recorded campaign impressions.")

