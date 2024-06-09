

# Create a Web Campaign

Using a web campaign, you can personalize various aspects of your website for
your users based on their behavior, affinities, preferences, location, or
other qualifying criteria. You can create web campaigns from templates in your
dataset. The templates provide a framework that defines the campaign
placement, copy and creative locations, and general campaign design.

### Required User Permissions

Permissions Needed  
---  
To create web campaigns: | A role with Campaigns Create/Edit permissions  
  
  1. Navigate to your website where you want to create the campaign.
  2. Click the **Extensions** icon in your browser’s toolbar and select **Salesforce Interactions SDK Launcher**.
  3. Enter your login credentials.
  4. Turn on the **Visual Editor** option.
  5. Select **Campaign > New Campaign** from the Visual Editor hexagon tiles.
  6. Enter a name for the campaign in the **New Campaign** field.
  7. Click the arrow next to **A/B Test**.
  8. Select either **A/B Test** or **Rule-Based Test** as the campaign type.
  9. If you select **A/B Test** as the campaign type:
    1. Use the sliders or enter a percentage of user traffic for the experience and the control.

![166e791e-416f-47c1-aeb9-511a0e058ca6]

Note Changing traffic percentage for an experience adjusts percentages on
other experiences to total 100% for the campaign. There are nuances that
determine how Personalization assigns a user to an experience. If you change
percentages after publishing a campaign and a prior campaign impression
statistic is logged, user and experience assignments stay the same. In this
case, the experience mirrors the impression statistic, and this mirroring
occurs only if Personalization receives an impression statistic. If the
sitemap is set up incorrectly and Personalization doesn’t receive an
impression statistic, Personalization can assign users to different
experiences.

    2. To add another experience, in the left navigation area, click the clone icon for Experience 1.
    3. To evenly distribute percentages, click **Redistribute**.
    4. Click **Save**.
  10. If you select Rule-Based Test as the campaign type:
    1. Enter a **Control** percentage. This percentage is the control group. This group of users meet the qualification criteria for the campaign and experiences but doesn’t see any campaign experiences.
    2. Click **+Add Rule** to add a qualification rule for an experience. 

![49b1c92f-98c1-4679-8496-cc7a134215f1]

Note These rules are specific to the experience.

    3. On the Experience Setup page, click **+Add Rule**.
    4. From the dialog that appears, select a category and then select one of its rules.
    5. Configure the parameters for the rule.
    6. To create another rule, click **+Add Rule** and repeat the process.
    7. To create an additional experience, click **Experiences+** and repeat the process.
    8. Click **Save**.
  11. To add a campaign-level rule, click **+Add Rule** in the **Campaign Targeting** section.
    1. Click **+Add Rule**.
    2. From the dialog that appears, select a category and then select one of its rules.
    3. Configure the parameters for the rule.
    4. To create another rule, click **+Add Rule** and repeat the process.
    5. Click **Save**.
  12. In the Experience 1 section, click **Add Template**.
    1. In the Select Template window, select the template you want to use for the first experience. The template appears under Experience 1.

![99307d5b-b42d-429b-a7be-c6d5cd43ad95]

Note Depending on the template, you can modify options, such as the image,
header text and styling, subheader text and styling, call-to-action text, and
call-to-action URL.

    2. Configure the template options as necessary.
    3. Click **Save**.
    4. To return to the campaign panel, click **All Experiences**.
  13. Add templates for any other experiences.
  14. Click **Save**.
  15. Test and publish your campaign.

#### See Also

  * [Test a Campaign Experience](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_experience_test.htm&language=en_US&type=5 "Although you can see your web campaign render as you create it, you can also test each campaign experience to see how it will appear to your intended audience. Testing the campaign experience allows you to view it, regardless of the qualification rules at the experience or campaign level. With campaign experience testing, you can review how the experience looks on the page.")
  * [Test a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_test.htm&language=en_US&type=5 "Use the campaign testing mode to test your campaigns before you publish them to ensure they display the way you intend.")
  * [Publish a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_publish.htm&language=en_US&type=5 "After you thoroughly test your campaign, you publish it to your website so that it’s visible to qualified users.")
  * [Campaign Statistics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_campaign_statistics.htm&language=en_US&type=5 "Use Campaign Statistics to measure the impact of your campaigns. The information available on the Campaign Statistics screen helps you analyze where you can make campaign changes to improve results.")
  * [Campaign Targeting Rules and Rule-based Tests](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_rule_based_test.htm&language=en_US&type=5 "Rules determine when, where, and how your campaigns display and who sees them. You can add rules when you create or edit a campaign at the campaign level for campaign targeting or when defining rule-based test experiences.")
  * [Web Campaign Types and Templates](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_types.htm&language=en_US&type=5 "Learn about different types of web campaigns and the available built-in templates.")

