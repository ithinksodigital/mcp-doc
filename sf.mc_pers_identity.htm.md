

# Unified Profiles and Identity Management

The concept of individual identity plays an essential role in personalizing
your customer experiences. Personalization aggregates all your customer data
in one place for analysis and personalization purposes. The aggregated
customer data helps you understand each of your customers on an individual
level so you can engage with them more effectively across your various
channels. Personalization uses specific identifiers to determine how to
process web events, API events, and channel events to identify and aggregate
users from various sources.

  * **[Unified Account Profile](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_account_profile.htm&language=en_US&type=5)**  
If you market to businesses, the Unified Account Profile displays aggregate
information that Personalization collects about a particular account. The
Unified Account Profile provides a comprehensive view of each of your accounts
according to the cross-channel interactions of customers and prospects.

  * **[Unified Customer Profile](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_customer_profile.htm&language=en_US&type=5)**  
The Unified Customer Profile provides a comprehensive view of each of your
users—visitors, customers, prospects, and subscribers—based on their
interactions with your various channels.

  * **[Unique User Profiles](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_about.htm&language=en_US&type=5)**  
To provide a unique experience for each of your customers, Marketing Cloud
Personalization identifies each customer with a user profile. However, as
users engage with your various channels, it’s possible to end up with multiple
user profiles for the same person. When identity data comes from different
sources, Personalization attempts to merge the information into a Unified
Customer Profile.

  * **[Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5)**  
Personalization’s identity system uses deterministic matching to create a
Unified Customer Profile for each of your customers. Specific identifiers,
called identity types, determine how to process web events, API events, and
channel events to identify users from various sources. Personalization
includes several built-in identity types, such as email address and customer
ID. If the built-in identity types don’t meet the needs of your organization,
you can create additional identity types.

  * **[Merge User Profiles](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_user_profile_merging.htm&language=en_US&type=5)**  
One of Personalization’s key goals is to identify each of your customers with
a Unified Customer Profile so that you can provide unique personalized
experiences. However, as users engage with your various channels, it’s
possible to end up with multiple user profiles for the same person. When
identity data comes from different sources, Personalization uses specific
identifiers to attempt to merge that data into a Unified Customer Profile.
There’s no way to split a merged user profile.

  * **[Merging Logic in the Salesforce Interactions SDK](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk_merging_logic.htm&language=en_US&type=5)**  
One of Personalization’s key goals is to identify each of your customers with
a Unified Customer Profile so that you can provide unique personalized
experiences. However, as users engage with your various channels, it’s
possible to end up with multiple user profiles for the same person. The
Marketing Cloud Personalization module of the Salesforce Interactions SDK
supports anonymous and named user profiles by using a first-party cookie to
track user behavior on your website. A user profile can transition from
anonymous to named based on the setup of the identity types in your Salesforce
Interactions SDK.

  * **[Set Up the Identity System for the Salesforce Interactions SDK](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk.htm&language=en_US&type=5)**  
To create unified customer profiles for each of your customers, use
Personalization’s identity system to configure the identifiers in the
Marketing Cloud Personalization module of the Salesforce Interactions SDK. To
merge user profiles from various sources, you designate an identity type to
use when matching users between channels. You can use multiple identifiers in
a web event.

  * **[Identity System Setup for Open Time Email](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_open_time_email.htm&language=en_US&type=5)**  
To create unified customer profiles for each of your customers, use
Personalization’s identity system to configure the identifiers in your Open
Time Email campaigns. To merge user profiles from various sources, you
designate an identity type to use when matching users between your email
service provider and Personalization. You can use only one identity type. If
you send multiple identifiers in an Open Time Email campaign, Personalization
ignores all but the designated identity type.

  * **[Identity System Setup for the Event API](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_event_api.htm&language=en_US&type=5)**  
With Personalization’s identity system, you can configure the identifiers in
the Event API to create Unified Customer Profiles for each of your customers.
To merge user profiles from various sources, you designate an identity type to
use when matching users between the Event API and Personalization. You can use
multiple identifiers in the Event API.

  * **[Identity System Setup for Mobile Apps](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_mobile_apps.htm&language=en_US&type=5)**  
Use the Personalization identity system to identify and merge user profiles in
your mobile app.

  * **[Troubleshooting Identity System Issues](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_troubleshooting.htm&language=en_US&type=5)**  
Review these troubleshooting tips if you’re experiencing general identity
system configuration issues or problems with user merges.

#### See Also

  * [ _Developer Documentation_ : "Determine Campaign Identity and Authentication Requirements" in Server-side Campaigns and Templates](https://developer.salesforce.com/docs/marketing/personalization/guide/server-side-campaigns-templates.html?q=Campaign%20Identity%20Authentication%20Requirements)

