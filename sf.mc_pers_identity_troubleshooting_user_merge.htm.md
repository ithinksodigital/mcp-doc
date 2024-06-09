

# Troubleshoot User Merges in the Identity System

If you’ve confirmed that your Personalization identity system is configured
correctly but users aren’t merging as expected, review these tips and
considerations.

### Required User Permissions

Permissions Needed  
---  
To configure the identity system: | A role with Administrator permissions  
  
Users can only merge one time per visit, regardless of how many devices
they’re active on. A “visit” starts from the first page view and ends after
the user reaches 30 minutes of inactivity on the site. For example, if a user
visits a homepage for the first time, exits, and then returns to the site 29
minutes later, the page views are still considered to be part of the first
visit.

  * Review these help topics about user merging to confirm whether the behavior you’re experiencing is expected: [Merge User Profiles](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_user_profile_merging.htm&language=en_US&type=5 "One of Personalization’s key goals is to identify each of your customers with a Unified Customer Profile so that you can provide unique personalized experiences. However, as users engage with your various channels, it’s possible to end up with multiple user profiles for the same person. When identity data comes from different sources, Personalization uses specific identifiers to attempt to merge that data into a Unified Customer Profile. There’s no way to split a merged user profile.") and [Merging Logic in the Salesforce Interactions SDK](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk_merging_logic.htm&language=en_US&type=5 "One of Personalization’s key goals is to identify each of your customers with a Unified Customer Profile so that you can provide unique personalized experiences. However, as users engage with your various channels, it’s possible to end up with multiple user profiles for the same person. The Marketing Cloud Personalization module of the Salesforce Interactions SDK supports anonymous and named user profiles by using a first-party cookie to track user behavior on your website. A user profile can transition from anonymous to named based on the setup of the identity types in your Salesforce Interactions SDK.").
  * Configure Identity Attributes before collecting any data in your implementation. 

![64d68165-49bc-4fa6-a462-092e6202010a]

Note If you have collected attribute values before turning an attribute type
into an Identity Attribute type, the existing values aren’t considered
identities.

  * After you configure your implementation and begin to collect data, don’t change the attribute an identity type is mapped to. This type of change can corrupt both the old and new identity types, and existing identity claims for involved identities become useless.
  * During implementation testing, user records might not merge as you expect, especially across many devices or with events from multiple sources that occur at once. The frequency of events from many channels or different identities can cause merges for single users, which are common in testing scenarios.

