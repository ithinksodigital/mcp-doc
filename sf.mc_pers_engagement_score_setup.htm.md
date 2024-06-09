

# Set Up an Engagement Score

The engagement score is an index that tracks how engaged your site visitors
and application users are. The score is based on several different factors
during a defined business cycle—visit information, actions, key performance
indicators (KPIs), and segment membership.

### Required User Permissions

Permissions Needed  
---  
To set up an engagement score: | Administrator  
  
  1. From the main navigation, select **Settings** | **Engagement**.
  2. For **Business Cycle** , enter the number of days of expected activity of site visitors or application users. A business cycle isn’t based on the calendar week. Instead, it begins the moment you change the number of days. Common business cycles are 7, 14, and 30 days, but a business cycle can be up to 90 days. For example, if it’s important for your customers to complete key activities one time per month, set your business cycle to 30 days.
  3. For **Weighting and Configuration** , use the sliders, enter a value, or use the arrows to set a percentage for each component. A 0 percentage omits the component from the engagement score calculation.
  4. To set the Weighting and Configuration**** component, click **Configure** next to the component.
  5. To configure the visit duration and number of actions for your engagement score, next to **Visits** , click **Configure**.
    1. Select how long a visitor must be logged in to be considered engaged. The target duration is based on your business cycle. For example, selecting 10 minutes means a fully engaged customer must be logged in for a minimum of 10 minutes during a business cycle. 
    2. Auto is the default visit duration target set by Personalization based on the average of all your active customers. Enter the number of total actions a visitor must complete in a visit (not a business cycle) to be considered engaged.
    3. Adjust the relative importance of **Visit Duration** against usage depth and its impact on the engagement score. If you consider visitors who spend a long time on your site or in your application to be highly engaged, assign a high weight to visit duration.
    4. Adjust the relative importance of **Usage Depth** against visit duration in terms of its impact on the engagement score. **Auto** is the default usage depth target set by Personalization based on the average of all your active customers. If engagement is directly related to how many actions a visitor completes on your site or in your application, assign a high weight to usage depth.
  6. To add actions and specify an action’s impact on the engagement score, next to **Actions** , click **Configure**.
    1. To add an action, click **Add Action**.
    2. Adjust the relative importance of an action in terms of its impact on the engagement score.

![04d20512-ea21-4a0d-bd59-20b26f2a7066]

Note Personalization looks at when a visitor last completed the action, how
many days in your business cycle visitors completed the action, and total
completions during your business cycle.

  7. To add KPIs and specify a KPI’s impact on the engagement score, next to KPIs, click **Configure**. KPI targets are based on actions that happen over the lifetime of the customer relationship, not on your business cycle. For example, you define engaged users as those having 50 connections. You create a KPI called “Connections” and set the target to 50. Any user who has reached 50 connections is fully engaged with that KPI, regardless of how long it took a customer to amass 50 connections.
    1. To add a KPI, click **Add KPI**.
    2. Set the KPI as a positive or negative indicator of engagement level.
    3. Adjust the relative importance of a KPI and its impact on the engagement score.
    4. Enter the usage depth target. **Auto** is the default usage depth target set by Personalization based on the average of all your active customers.
  8. To add segments and specify a segment’s impact on the engagement score, next to Segments, click **Configure**. Include segments (except segments based on engagement score, which can’t be used) that are important to your engagement score. For example, add specific groups of visitors (such as premium subscribers) or users (such as administrators) that you want to score higher than others. If you want both administrators and premium subscribers of your product to score higher, create a segment of these users and add the segment to the engagement score. 
    1. To add a segment, click **Add Segment**.
    2. Set the segment as a positive or negative indicator of engagement level.
    3. Adjust the relative importance of a segment in terms of its impact on the engagement score.
  9. When done, click **Save and Recalculate**.

