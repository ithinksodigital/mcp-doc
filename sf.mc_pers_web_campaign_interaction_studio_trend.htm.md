

# Use Marketing Cloud Personalization Trends

Personalization Trends uses social validation to increase conversions. Most
consumers are overwhelmed by the product choices available to them and can
find it challenging to confidently buy products online. Use view and purchase
counters to influence users of your website in real time and build confidence
in their product selections.

### Required User Permissions

Permissions Needed  
---  
To use trends: | A role with Templates > Create/Edit permissions  
  
Before you can build campaigns using trends:

  * You must enable the feature in your dataset.
  * You need a developer to configure the IS Trends template so you can use it to create a web campaign.

Using an item ID and a designated number of lookback minutes, Personalization
returns the number of views and recent purchases for the item within that
period.

  1. From the main navigation menu, select **Settings > General Setup**.
  2. Click the **Advanced Options** arrow.
  3. Select the check box next to **Enable IS Trends**. 
  4. Click **Save**.
  5. Create a web campaign. For more information, see [Create a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_create.htm&language=en_US&type=5 "Using a web campaign, you can personalize various aspects of your website for your users based on their behavior, affinities, preferences, location, or other qualifying criteria. You can create web campaigns from templates in your dataset. The templates provide a framework that defines the campaign placement, copy and creative locations, and general campaign design.").
  6. Select the **IS Trends** template for Experience 1.
  7. Configure the following fields:

Field | Description  
---|---  
**Purchases Text** | This text displays after the numerical value for the item’s purchases, such as "recently purchased."  
**Visitors Text** | This text displays after the numerical value for the item’s views, such as "customers currently viewing."  
  
  8. Finish creating your campaign, then test and publish it.

![f4f054d5-5ef2-4f44-a1d5-94d16180a338]

Note If the content zone you’re targeting appears on non-PDP pages, add page
targeting rules to ensure that the campaign appears only on a PDP.

#### See Also

  * [Test a Campaign Experience](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_experience_test.htm&language=en_US&type=5 "Although you can see your web campaign render as you create it, you can also test each campaign experience to see how it will appear to your intended audience. Testing the campaign experience allows you to view it, regardless of the qualification rules at the experience or campaign level. With campaign experience testing, you can review how the experience looks on the page.")
  * [Test a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_test.htm&language=en_US&type=5 "Use the campaign testing mode to test your campaigns before you publish them to ensure they display the way you intend.")
  * [Publish a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_publish.htm&language=en_US&type=5 "After you thoroughly test your campaign, you publish it to your website so that it’s visible to qualified users.")
  * [Campaign Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics.htm&language=en_US&type=5 "Use Campaign Statistics to measure the impact of your campaigns. The information available on the Campaign Statistics screen helps you analyze where you can make campaign changes to improve results.")
  * [ _Developer Docs_ : Marketing Cloud Personalization Trends](https://developer.salesforce.com/docs/marketing/personalization/guide/is-trends.html)

