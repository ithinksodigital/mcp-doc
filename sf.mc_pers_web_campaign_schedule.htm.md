

# Schedule a Web Campaign

You can schedule your web campaigns to ensure that personalized experiences
only display between certain dates, during certain days of the week, or even
during certain hours of the day. This increased control helps you further
target and tailor personalized content to your users across various channels.

### Required User Permissions

Permissions Needed  
---  
To schedule web campaigns: | A role with Campaigns Create/Edit permissions  
  
  1. Navigate to your website that has the campaign you want to schedule.
  2. Click the **Extensions** icon in your browser’s toolbar and select **Salesforce Interactions SDK Launcher**.
  3. Enter your login credentials.
  4. Turn on the **Visual Editor** option.
  5. Select **Campaign > View List** from the Visual Editor hexagon tiles.
  6. Click the **Edit Campaign** button for the web campaign you want to schedule.
  7. Click the arrow in the **Campaign Targeting** section.
  8. Click **+Add Rule**.
  9. From the dialog that appears, select **Scheduling** as the category.
  10. Select and configure a scheduling rule with these options. **Date Range** | Schedules a campaign to run today, on or after a specific date and time, on or before a specific date and time, or between specific dates and times. The Date Range rule uses your local time. Marketing Cloud Personalization displays your time zone next to each date/time field.  
---|---  
**Time of Day** | Schedules a campaign to run on specific days of the week and during specific hours of the day. This rule uses UTC time. Personalization displays “UTC” next to each time dropdown.  
  11. Click **Save**.

![9c2c8776-adc9-4624-8e44-0023bddaf7c9]

Example

If a campaign creator in Boston schedules a campaign using the **Date Range**
rule, the time displays as Eastern time and the campaign runs accordingly. If
a colleague in San Francisco views the campaign in the app, the times display
in Pacific time. So, if the Boston-based campaign creator sets the time to
9:00 AM ET on October 31, the San Francisco-based colleague sees it as 6:00 AM
PT on October 31.

If the Boston campaign creator schedules a campaign to run Monday–Friday
between 9:00 AM and 5:00 PM using the **Time of Day** rule, they must convert
Eastern time to UTC time. So they enter 1:00 PM and 9:00 PM as the
corresponding UTC values. The San Francisco-based colleague sees those same
values.

