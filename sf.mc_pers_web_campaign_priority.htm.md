

# Manage Web Campaign Priorities

When a customer qualifies for multiple web campaigns that target the same
content zone and match a particular page or action, Marketing Cloud
Personalization shows only one of those campaigns. You can adjust the priority
values for campaigns to determine which campaign displays. Campaigns with a
higher priority value have precedence. When campaigns have the same priority
value, the campaign that was created first has precedence.

### Required User Permissions

Permissions Needed  
---  
To manage campaign priorities: | A role with Campaigns Create/Edit permissions  
  
Campaign priority requires that a content zone is present to select between
campaigns that a customer qualifies for. Personalization doesn’t use priority
for server-side campaigns that don’t have content zones. Instead,
Personalization returns all campaigns that a user qualifies for.

![482a0711-5c59-4c9c-87b6-06e2ea4316a8]

Note For rule-based campaigns, experiences are also prioritized. If a user
qualifies for a campaign and qualifies for multiple experiences, the
experience at the top of the list has the highest priority. You can reorder
campaign experiences in the campaign editor.

  1. From the **Channels & Campaigns** section of the main navigation, select **Web > Web Campaigns**.
  2. Select the campaign. The campaign’s priority appears in the **Overview** tab of the detail pane.
  3. To change the priority, double-click the campaign.
  4. In the campaign editor, click the arrow next to the campaign type (**A/B Test** or **Rule-Based Test**).
  5. Adjust the value of the **Priority** field by using the arrows or by entering a number.

![915f5318-1c08-47d5-bae2-1d62353b192f]

Note The campaign with the highest value has the highest priority. To ensure a
particular campaign always displays before other campaigns that conflict,
assign a high number as its priority. Priority values can be negative, and the
default priority value is 0.

  6. Click **Save**.

#### See Also

  * [Web Campaign Experiences](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_experience.htm&language=en_US&type=5 "A web campaign experience is the experience an individual customer has with a particular web personalization or activation campaign. You can use experiences to create different personalization results within the same campaign.")
  * [Create a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_create.htm&language=en_US&type=5 "Using a web campaign, you can personalize various aspects of your website for your users based on their behavior, affinities, preferences, location, or other qualifying criteria. You can create web campaigns from templates in your dataset. The templates provide a framework that defines the campaign placement, copy and creative locations, and general campaign design.")

