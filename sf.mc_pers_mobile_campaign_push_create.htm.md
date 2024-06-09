

# Create a Mobile Push Campaign

Create a mobile push campaign to send push notifications to your iOS and
Android app users.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create or edit Mobile Push campaigns: | A role with Campaign Create/Edit permissions  
To publish or delete Mobile Push campaigns: | A role with Campaign Publish/Delete permissions  
  
  1. In the **Channels & Campaigns** section of the main navigation, select **Mobile** | **Mobile Push Campaigns**.
  2. Click **New Campaign**.
  3. Select **Setup** | **Campaign Settings**.
  4. (Optional) Select a **Goal**.
  5. (Optional) Select a **Measure of Success**.
  6. Enter one or more **Target Applications** to receive campaign push notifications.
  7. For iOS apps that use Apple Push Notification service (APNs), select whether to send push notifications with an APNs production certificate, a sandbox certificate, or both.
  8. In **Setup,** select **Send Options**.
  9. Select and configure the **Trigger Type**. 

A trigger sends the push notification. The configuration options that appear
depend on the trigger type you select. Trigger types are user-driven (segment,
cart, browse, event) and catalog-driven (new, returning, expiring, low stock,
price reduction). For information about trigger types and associated
configuration options, see [User
Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_user.htm&language=en_US&type=5
"A user trigger activates a campaign based on user behavior.") and [Catalog
Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_catalog.htm&language=en_US&type=5
"A catalog trigger activates a campaign based on updates or changes to item
data in your catalog. The trigger activates after a change in your catalog,
but what drives the trigger is the amount of time the user views an item
before the catalog change occurs.").

  10. In the **Subscriber List / Segment** section, select a segment or subscriber list that you want to send the campaign to.
  11. (Optional) Configure any of the following send options.

Setting | Description  
---|---  
**Required Segments** | Select one or more segments that qualify users to receive the campaign.  
**Excluded Segments** | Select one or more segments that disqualify users from receiving the campaign.  
**Mobile Push Frequency Limits** | Set campaign-specific frequency limits, which are in addition to the global frequency limits.  
  
  12. To add a campaign experience, click **+Experience** and configure the new experience.
  13. Close the Setup panel.
  14. In the Message Content panel, enter a **Title** for Android mobile app users only. If the field is empty or if the user is on an iOS device, mobile app users see the name of the mobile app.
  15. Enter the message **Body** that you want mobile app users to see when they expand the notification. 

![41f4c13a-e285-4c90-ac5d-9183d9b4945d]

Note You can use dynamic values in the Body field. For more information, see
[Use Dynamic Values in Mobile
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_dynamic_values.htm&language=en_US&type=5
"You can add dynamic values, such as the mobile app user’s name, location, and
email, to all mobile campaign types.").

As you’re typing, you can see a preview of the campaign as it appears on the
selected device. You can change the selected device in the **Preview**
dropdown.

  16. (Optional) Click **Show Advanced Settings**.
  17. (Optional) For both iOS and Android devices, you can configure these advanced settings.

Setting | Description  
---|---  
**Time To Live** | The amount of time FCN or APNs attempts to deliver the notification to offline or unreachable devices. Time to live is shared across all apps and devices in the campaign. A value of “0” means Personalization doesn’t attempt delivery again for unreachable devices.  
**Sound** | The app sound filename or identifier. An empty value means don’t play a sound. The default value uses the device’s default system sound. You can define a different sound for each app.  
**Additional Data** | A set of key or value pairs that contain any additional info you add, but typically convey user or product information. You can use dynamic values. You can define different data for each app.  
  
  18. (Optional) For Android-specific devices, you can configure these advanced settings.

Setting | Description  
---|---  
**Click Action** | The action that displays and consumes any additional data when the user opens the push notification.  
**Icon** | The app icon filename or identifier the campaign uses.  
**LED Color** | The color the campaign flashes using the device's LEDs.  
**Collapse Key** , **Channel ID** , **Tag** , **Restricted package name** | Refer to the Firebase programming guide.  
  
  19. (Optional) For iOS-specific devices, you can configure these advanced settings.

Setting | Description  
---|---  
**Badge** | The number to associate with the app icon's badge. An empty value has no effect on the badge. A value of “0” clears the badge.  
**Category** , **Thread ID** | Refer to the APNs programming guide.  
  
  20. Add mobile campaign rules as needed. For more information, see [Use Mobile Campaign Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_rules.htm&language=en_US&type=5 "A critical part of a good personalization strategy is giving mobile app users information related to what they’re doing or feeling in the moment. Use campaign, experience, and message rules to deliver your message to the right person at the best time for them.").

![aaacefd0-0b97-4945-a938-818d72527d5c]

Example Multi-app Scenarios

Three scenarios of multi-app targets are:

  * Android and iOS versions of the same mobile app
  * Internal or development and production environments for the same mobile app
  * Android and iOS versions of development and production environments for the same mobile app

You can configure target apps in Campaign Settings.

Before you publish a Mobile Push campaign, you must generate and upload a
certificate for APNs or Firebase Cloud Messaging (FCM). For instructions, see
[Complete Mobile Push
Setup](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_push_setup.htm&language=en_US&type=5
"Before you publish a Mobile Push campaign, you must generate and upload a
certificate for Apple Push Notification service \(APNs\) or Firebase Cloud
Messaging \(FCM\). If you enter credentials for both APNs and FCM, you must
pick one when you add the app to a Mobile Push campaign. To prevent duplicate
notifications, Personalization only sends to one platform.").

