

# Add Mobile Experience Targeting Rules

Experience-level rules are available only for rule-based campaigns. They
control qualification criteria of campaign experiences based on segments and
the actions of mobile app users.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To add mobile campaign rules: | A role with Campaign Create/Edit permissions  
  
Add the rules that support your campaign strategy. If you include multiple
rules in the same experience, to qualify for the experience, mobile app users
must satisfy all rules regardless of the order (and logic). For a list of
mobile experience rules, see [Mobile Experience-Level
Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_experience_level_rules.htm&language=en_US&type=5
"For all types of mobile campaigns, if you set experience-level rules, each
experience needs a qualifying rule. Mobile app users who qualify for the
campaign see the first experience in the list for which they qualify. If you
set a control percentage, it applies only to users who have qualified for the
experience.").

  1. Create or edit a Mobile In-App Message, Mobile Data, or Mobile Push campaign.
  2. Click **Setup**.
  3. Select **Experiences**.
  4. Set the **Test Mode** to **Rule-Based**.
  5. Set the **Control Mode** :

Mode | Description  
---|---  
**Percentage** | Specify a percentage of qualified users who see the original experience.  
**Experience** | Specify an experience as the control group.  
  
  6. Select each experience that you want to apply rules to.
  7. In the **Experience Level Rules** section, click **+New Rule** for the desired group of rules.
  8. To select a rule category, click **Select Rule Type**.
  9. Complete the other options, which vary by category and rule.
  10. To add additional rules for the same experience, click **+New Rule**.
  11. Select each additional experience and add at least one rule.
  12. To save your campaign, click **Save**.

Review targeting rule options for campaigns and messages against your strategy
and goals for your campaign. Add any that support the success of your
campaign.

#### See Also

  * [Create a Mobile Push Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_push.htm&language=en_US&type=5 "Create a Mobile Push campaign to send push notifications to your iOS and Android app users. For Android users, the campaigns support Firebase Cloud Messaging \(FCM\) and require an app integration with the Personalization Android SDK 1.3 and later. For iOS users, the campaigns support Apple Push Notification service \(APNs\) and Firebase Cloud Messaging \(FCM\), and require an app integration with Personalization iOS SDK 1.3 and later.")
  * [Create a Mobile In-App Message Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_in_app_message.htm&language=en_US&type=5 "You can use a Mobile In-App Message campaign to build and deploy messages within mobile apps. Mobile In-App Message campaigns are similar to the infobar messages you can add to your website. You build, manage, and deploy Mobile In-App Message campaigns from within Personalization so you get the same real-time data and personalization you rely on with your other campaigns. You don't need an engineer's help or App Store approval to deploy new or changed messages.")
  * [Create a Mobile Data Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_data.htm&language=en_US&type=5 "Create Mobile Data campaigns so your iOS and Android apps can process Personalization campaign data. Personalization triggers campaigns and delivers the data to your app.")

