

# About Mobile Campaigns

There are three types of mobile campaigns you can create with Marketing Cloud
Personalization: In-App Message, Push, and Data campaigns.

### Required Editions

Available in: Premium Edition  
---  
  
## Mobile In-App Message Campaigns

Mobile In-App Message campaigns offer functionality similar to basic web
messages, including:

  * Format background color, position, and text 
  * Preview messages on different iOS devices
  * Link to in-app content, external sites, email, or another app, such as Maps
  * Insert dynamic content for your message and add data fields, such as username or product name 
  * Target with segment data, including screen views, actions, and locations
  * Target different audiences within the same campaign using multiple experiences

If you want to use Mobile In-App Message campaigns for inline page changes and
recommendations, you must configure an API connection. Push notifications
aren’t available in Mobile In-App Message campaigns.

## Mobile Push Campaigns

Use Mobile Push campaigns to send push notifications to your iOS and Android
app users.

  * [Android](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-android-sdk/v1.3.0/push-notifications.html)—Supports Firebase; Requires app integration with Personalization Android SDK 1.3 and later.
  * [iOS](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-ios-sdk/push-notifications.html)—Supports APNs and Firebase; Requires app integration with Personalization iOS SDK 1.3 and later

The [Push
Notifications](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-
ios-sdk/push-notifications.html) section in the Personalization SDK
documentation covers:

    * APNs and Firebase configuration
    * Credentials
    * Personalization SDK configuration
    * Advanced details about mobile push notifications in Personalization

## Mobile Data Campaigns

Create Mobile Data campaigns so your iOS and Android apps can process
Personalization campaign data. Personalization triggers campaigns and delivers
the data to your app.

How does it work? A developer writes campaign handlers as app code to flexibly
consume campaign data. After that code is in place, Mobile Data campaigns can
deliver dynamic content to your app. At a high level, the process has five
steps:

  * The mobile app code registers campaign handlers for content zones.
  * The mobile app's Personalization integration sends events, such as screen or product views, to Personalization.
  * The events trigger Mobile Data campaigns.
  * The campaign data calls the campaign handler code in JSON format to process and render the mobile campaign.
  * The mobile app calls Personalization APIs to track impressions, dismissals, and clicks.

You can use Mobile Data campaigns for:

Use | Description  
---|---  
Messaging | If your app already has its own banner or infobar system, you can use Personalization campaigns to feed information about sales, promotions, user credit or points, and other data.  
Recommendations | Apps can have content zones or targets to display recommended items. A campaign can deliver recommendations to the campaign handler code.  
  
#### See Also

  * [ _Developer Documentation_ : Personalization Mobile Integrations](https://developer.salesforce.com/docs/marketing/personalization/guide/mobile-integration.html)

