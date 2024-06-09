

# Engagement Score Usage

After your engagement score is set up and synced, you can view user and
account engagement scores in Personalization.

## Engagement Score Components

Your engagement score has the following major components.

Item | Description  
---|---  
Visits | Visitors are scored on their visit statistics, including duration and depth (how many different actions were completed during the visit).  
Actions | The actions customers take with your application or on your site.  
KPI | Sum totals of important actions. For example, a social media site can have a Key Performance Indicator (KPI) for user connections. You configure each KPI as a user attribute integer.  
Segments | Visitor membership in behavior-based segments. Only visitors in the segment have points added to or subtracted from their engagement score.  
  
## Basis for the Engagement Score

Your engagement score is based on previous visits and decays over time. If a
visitor hasn’t visited your site for an entire business cycle, the engagement
score drops to half of what it was on the last visit. If a visitor hasn’t
visited your site for two business cycles, the engagement score drops to 0.
When a visitor’s engagement score drops to zero, it stops affecting the
overall engagement score of your account, segment, and entire dataset.

## Example Graph of Engagement Score Decay Over Time

The graph shows the decay of the engagement score of two users, A and B, over
a period of 70 days.

![0e2376d5-243f-4b8a-bbc3-1c9fadbfdf23]

User A’s last visit is on day 1 of the graph. She has a score of 100% because
she meets all the defined criteria for the engagement score. This criteria is
based on visits, actions performed, KPI values, and joined segments. If the
business cycle is set to 30 days, User A’s engagement score drops after 30
days to 50% of what it was on day 1. Sixty days after her last visit, her
engagement score is 0. At that point she’s considered inactive and doesn’t
contribute to the overall engagement score.

User B’s last visit is on day 10 of the graph. His engagement score was only
60% at the end of that day. Thirty days later, on day 40, he has an engagement
score of 30% (half of the original score). Thirty days after that, or twice
the business cycle, he has an engagement score of 0 and no longer contributes
to the overall engagement score. The decay isn’t linear and is slower at the
beginning and end of the time frame and faster near the end of one business
cycle.

