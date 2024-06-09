

# Create a Segment

A segment is a real-time grouping of users, or accounts, based on criteria you
define using a set of segment categories and rules.

### Required User Permissions

Permissions Needed  
---  
To create a segment: | A role with Segments Create/Edit permissions  
  
![a2388708-36f0-43a8-b2ae-595224c25ec6]

Note If you want to maintain the structure of an existing segment and only
make minor modifications, you can clone that existing segment instead of
creating a segment.

  1. In the **Audiences** section of the main navigation, select **User Segments** | **User Segments**.

If you have accounts configured for your dataset, you also have the option to create account segments by selecting **Account Segments** | **Account Segments**.

  2. Click **New Segment**.
  3. Enter a **Segment Name** that describes its purpose.
  4. Select a category from the **Select Category** dropdown to use for the first rule in your segment. 

Category | Description  
---|---  
Campaign | You can create segments based on whether a user views or interacts with a campaign, and how often and how recently. You can also create segments for A/B testing.  
Action | You can create segments based on whether a user performs a specific action or a group of actions, and how often and how recently. Actions vary by dataset. You can view the actions for your dataset by selecting **Reports** | **Actions**.  
Subscription | You can create segments based on a subscription level or where a user or account is in the lifecycle of a subscription. The location of this segment rule option is dependent on your dataset configuration. The Personalization system typically tracks subscriptions for B2B sites at the account level, and at the user level for B2C sites. This category is available for demand-generation sites only.  
Visits | You can create segments based on a user’s visit data, including visit count, visit duration, visit recency, visit source, time since first visit, the originating referrer, and whether the user is anonymous.  
Location | You can create segments based on a user’s location, including ZIP code (US only), city, metro region, state or region, and country. Additionally, you can segment on the distance from a ZIP code (US only), city, or latitude-longitude coordinates. You can also use the user’s ISP to create segments. If you have B2B Detect, you can also create segments based on company name or industry.  
Metrics | You can create segments for certain metrics based on information that you provide during your implementation. You can also segment on text attributes (attribute equals, or attribute exists).  
Third Party | You can create a segment for users that have the defined third-party application ID. This option is available only if you have a first-class third-party email provider syncing with the Personalization system.  
Items | You can create segments based on items in your catalog, such as products, categories, articles, and keywords, and the amount spent, added to cart, or abandoned.  
  
  5. Select the **Rule** for the category.
  6. Configure the applicable parameters for the rule.
  7. To add additional rules, click **New Rule**.

![7cac7068-8b0d-45b8-be37-df5d167fed93]

Note Each rule appears as a separate column in the Segment Details, and in the
CSV file when you export the segment.

  8. Select a logical operator for the additional rule:

Operator | Description  
---|---  
AND | Membership in the segment requires that a user meets all the criteria for all rules.  
OR | Membership in the segment requires that a user meets one or more of the criteria for the rules.  
  
![db440a5e-e3c0-4dee-9f3e-eeb493111fb0]

Note To include both AND and OR logical operators in your segment rules,
create additional groups of rules.

  9. To add another group of rules, click **New Group**.
  10. Create additional rules as necessary.
  11. To send a daily email report that includes the current membership link, and a list and count of the users added and removed, enter an email address in the **Email Reporting** field. 
  12. Click **Save**.

![f37bb7e2-ae30-4a00-a6ac-6f135c367e8e]

Tip Click **New Folder** to create folders that logically group segments so
you can find them quickly in Filters and Goals and in Campaign Statistics. For
example, segments with users who click through an email can all be in a folder
named “Clickthrough." Drag a user segment to add it to a folder.

