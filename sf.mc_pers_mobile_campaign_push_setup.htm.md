

# Complete Mobile Push Setup

Before you publish a Mobile Push campaign, you must generate and upload a
certificate for Apple Push Notification service (APNs) or Firebase Cloud
Messaging (FCM). If you enter credentials for both APNs and FCM, you must pick
one when you add the app to a Mobile Push campaign. To prevent duplicate
notifications, Personalization only sends to one platform.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create and upload APNs and Firebase credentials for a mobile app: | A role with Administrator permissions  
  
  1. Complete APNs and Firebase configuration before uploading APNs and Firebase credentials in the push notification setup.
  2. In the **Channels & Campaigns** section of the main navigation, select **Mobile**.
  3. In the **Mobile App Setup** section, select your existing Personalization-enabled mobile app.
  4. Click **Mobile Push Setup**.
  5. Enter or upload the credentials for Android, iOS, or both:
    1. For **Android** : Enter or paste your Firebase **Legacy Server Key** (as described in [Push Notifications (Android)](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-android-sdk/v1.3.0/push-notifications.html)) and click **Save**. 
    2. For **iOS** : For more information, see the [Push Notifications (iOS)](https://developer.salesforce.com/docs/marketing/personalization/references/personalization-ios-sdk/push-notifications.html).
    3. For APNs: Generate the app's APNs certificates, if you don't have them.
    4. For each sandbox or production certificate: Save the certificate and private key as a .p12 file, enter the optional .p12 file password, and click **Upload p12 File** and upload the .p12 certificate.

![18223f9e-5fb8-4d1b-a6cf-a9e4a18ffde6]

    5. For Firebase: Enter or paste your **Legacy Server Key** and click **Save** , then provide your APNs credentials to Firebase. 

![bf9d20bf-9c83-42d4-bacb-830dcb944abb]

For more information, see [Set up a Firebase Cloud Messaging client app on
Apple platforms](https://firebase.google.com/docs/cloud-messaging/ios/certs).

