

# Unique User Profiles

To provide a unique experience for each of your customers, Marketing Cloud
Personalization identifies each customer with a user profile. However, as
users engage with your various channels, it’s possible to end up with multiple
user profiles for the same person. When identity data comes from different
sources, Personalization attempts to merge the information into a Unified
Customer Profile.

Creating a unique user profile is easy when the sources contain clear identity
information, such as a customer ID or email address. However, each user
doesn’t always have a clear identifier for every interaction within each
channel. For instance, in these examples the separate user profiles each
contain important customer data, but none has enough information to provide a
user’s complete identity.

  * A retail shopper makes several in-store purchases by using their loyalty number. The retailer has the shopper’s name and other identity information through the loyalty program, along with a history of in-store purchases. Later, the shopper browses the store’s ecommerce site, but doesn’t make a purchase or identify themselves in any way. As a result, their named in-store profile remains separate from their anonymous website profile.
  * To download a report, a website visitor completes a form that includes their name and email address. The organization can now identify the visitor when they’re on their website. Later, the person uses a different browser to visit the website, which creates a second profile that captures their website activity as an anonymous visitor.
  * A bank customer receives an email with a mortgage offer, reads it, and clicks through to the bank’s website for more information. The next day, the customer contacts the bank’s call center to discuss the offer. In this scenario, they can have three separate profiles based on their interactions with the bank’s email, web, and call center systems.

## Types of Users

Marketing Cloud Personalization identifies two types of users (or visitors) in
Marketing Cloud Personalization —anonymous (or unknown) and named (or known).
Whether anonymous or named, Marketing Cloud Personalization creates a profile
ID for all users. How the Personalization system distinguishes between the two
types depends on the information it can gather about them. To be considered a
known user, in addition to their assigned profile ID, a user must be
identified by at least one other identity value.

User Type | Description  
---|---  
Anonymous (Unknown) | A user that isn’t yet validated as known by Marketing Cloud Personalization. An unknown user can have a profile ID, but this identity value isn’t enough to consider the user known.  
Named (Known) | A user that is validated by Marketing Cloud Personalization using one or more accepted identities, such as an email address, phone number, or mailing address, along with their Personalization profile ID.  
  
## Profile Merging

Personalization constantly monitors identity information from your users’
interactions with your channels. When identity data becomes available,
Personalization uses deterministic matching to attempt to assign that data to
an existing user profile. If two or more user profiles represent the same
identity, Personalization merges them to create a Unified Customer Profile for
that person.

For example, Mary Smith is a customer with one named user profile and one
anonymous user profile in Personalization. Her named user profile incorporates
data from several different channels—retail store, call center, and mobile
app. Mary also has an anonymous user profile from the company’s website
because she’s never identified herself when browsing the website using her
laptop. Personalization merges Mary’s two user profiles when she identifies
her anonymous user profile while on her laptop, such as by clicking through
from an email to the website.

Personalization merges user profiles based on clear, unique identifiers, such
as a system ID or an email address. If a person visits a website multiple
times but doesn’t provide identity information, their user profile remains
anonymous. If the anonymous person provides their email address,
Personalization updates the anonymous user profile to a named user profile and
merges the anonymous sessions from the same cookie to create a Unified
Customer Profile.

## Unified Customer Profiles

Regardless of whether a person is named or anonymous, a Unified Customer
Profile defines a customer's identity using data collected from a variety of
sources across all channels. This single, comprehensive user profile is
central to Personalization and is the foundation of campaign personalization
and data analysis.

The Unified Customer Profile includes data that helps you understand your
prospects and customers. This data can include purchases, browsing history,
email interactions, subscriptions, loyalty membership, interests, preferences,
browser type, location, and demographics. The Unified Customer Profile also
includes identity data elements that provide connections between different
user profiles. Identity data elements include cookies, email address, full
name, physical address, phone number, and system ID.

Using Unified Customer Profiles you can better determine:

  * Whether a customer qualifies for a promotion
  * Which products and content to recommend
  * Which channel to use for communications
  * When to send an email

## Identity System and Types

To create a Unified Customer Profile, Personalization uses built-in identity
types, such as email address and customer ID, to determine how to merge user
profiles from various sources. If the built-in identity types don’t meet your
needs, you can create additional identity types.

You set up the identity system during implementation before collecting data.

How you use the identity system for identity lookup and merging user profiles
depends on the channels and systems you’re using.

Channel or System | Configuration Details  
---|---  
Web events | Configure an additional setting for your sitemap to include identity types. See [Set Up the Identity System for the Salesforce Interactions SDK](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk.htm&language=en_US&type=5 "To create unified customer profiles for each of your customers, use Personalization’s identity system to configure the identifiers in the Marketing Cloud Personalization module of the Salesforce Interactions SDK. To merge user profiles from various sources, you designate an identity type to use when matching users between channels. You can use multiple identifiers in a web event.").  
ETL system | Personalization’s ETL system provides APIs for identity lookup and merging user profiles based on a list of identity types and attributes in a CSV file. User ETL and Transaction ETL jobs use these APIs to determine whether to map incoming data to an existing user profile in Personalization. See User ETL, Transaction ETL, and External Email Campaign Events ETL documentation for details.  
Event API jobs | Configure an additional setting. See [Identity System Setup for the Event API](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_event_api.htm&language=en_US&type=5 "With Personalization’s identity system, you can configure the identifiers in the Event API to create Unified Customer Profiles for each of your customers. To merge user profiles from various sources, you designate an identity type to use when matching users between the Event API and Personalization. You can use multiple identifiers in the Event API.").  
Mobile Apps | Configure an additional setting. See [Identity System Setup for Mobile Apps](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_mobile_apps.htm&language=en_US&type=5 "Use the Personalization identity system to identify and merge user profiles in your mobile app.").  
Open Time Email Campaigns | Configure an additional setting. See [Identity System Setup for Open Time Email](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_open_time_email.htm&language=en_US&type=5 "To create unified customer profiles for each of your customers, use Personalization’s identity system to configure the identifiers in your Open Time Email campaigns. To merge user profiles from various sources, you designate an identity type to use when matching users between your email service provider and Personalization. You can use only one identity type. If you send multiple identifiers in an Open Time Email campaign, Personalization ignores all but the designated identity type.").

