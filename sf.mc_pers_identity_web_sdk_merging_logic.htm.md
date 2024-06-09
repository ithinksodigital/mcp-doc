

# Merging Logic in the Salesforce Interactions SDK

One of Personalization’s key goals is to identify each of your customers with
a Unified Customer Profile so that you can provide unique personalized
experiences. However, as users engage with your various channels, it’s
possible to end up with multiple user profiles for the same person. The
Marketing Cloud Personalization module of the Salesforce Interactions SDK
supports anonymous and named user profiles by using a first-party cookie to
track user behavior on your website. A user profile can transition from
anonymous to named based on the setup of the identity types in your Salesforce
Interactions SDK.

## Anonymous User Profiles

The Marketing Cloud Personalization module of the Salesforce Interactions SDK
generates an anonymous ID for all events, but assigns an anonymous ID for the
user’s identity on the visitor’s initial visit, and only when the event
contains no identity types. Once assigned, the anonymous ID remains associated
with that visitor and browser until explicitly removed or timed out. For
anonymous events, Personalization uses its anonymous ID to determine whether
the events match the anonymous IDs of any existing user profiles, or whether a
new user generated the event.

Example Scenarios | Analysis | Resolution  
---|---|---  
An organization is using the Email Address identity type in its Web SDK.Personalization receives a page view event from a visitor without an email address. | The event doesn’t contain an anonymous ID. | The identity system assigns the website visitor an anonymous ID. Personalization creates a new anonymous user profile, and assigns the event data to that profile.  
An organization is using the Email Address identity type in its Web SDK.Personalization receives a page view event from a visitor without an email address. | The event contains an anonymous ID that matches an existing anonymous user profile. | Personalization recognizes that the event is from a returning anonymous user and assigns the event to that user’s profile.  
  
## Named User Profiles

If one or more identity types are present in a web event, Personalization
considers it a named event. Personalization uses the identity types to either
assign that event to an existing user profile or create a user profile for it.
An anonymous profile can become a named profile through this identity lookup
and merging process.

Example Scenarios | Analysis | Resolution  
---|---|---  
An organization is using the Email Address identity type in its Web SDK.Personalization receives a page view event that contains an email address value. | The email address value doesn’t match any existing user profiles. However, the anonymous ID of the event matches the ID of an existing anonymous user profile. | Personalization assigns the event data to the existing anonymous user profile. The event’s email address value changes the anonymous user profile to a named user profile.  
An organization is using the Email Address identity type in its Web SDK.Personalization receives a page view event that contains an email address value. | The email address value matches an existing named user profile. | Personalization assigns the event to the existing named user profile.  
Personalization receives an event from the Internet with two identity types: Email Address and Customer ID. | Two user profiles exist with identifiers that match the ones in the event. One profile has a matching email address and the other profile has a matching customer ID.In the user profile with the matching customer ID, the email address isn’t the same as the Email Address value in the event. | Personalization merges the two existing user profiles. Because the email address from the incoming event has the latest timestamp, Personalization retains that email address.  
  
## User Profiles from Different Devices

Personalization can merge multiple user profiles that result from the same
individual using different devices. For example, if a person visits your
website from a desktop computer and from a mobile device, that individual has
two anonymous IDs. Personalization tracks their behavior in two separate
anonymous user profiles. When a named event occurs on each device, like a
login or a purchase, the anonymous user profiles become named user profiles
and have a matching identity. Personalization can then merge the two named
user profiles into a unified customer profile and combines their histories.

Example Scenario | Analysis | Resolution  
---|---|---  
An organization is using the Email Address identity type in its Web SDK. A user visits their website from a desktop computer, and Personalization assigns them an anonymous ID.Later, the same person visits the website from a mobile device, and Personalization assigns them a second anonymous ID.The visitor then completes a login action from the desktop computer and from their mobile device. | When the visitor completes a login action from each device assigned an anonymous ID, Personalization captures the email address and sends it with the login events from each device. | Personalization uses the Email Address value to merge both anonymous user profiles into a single named user profile with the combined behavioral history from both user profiles.

