

# September 2021 Features in Interaction Studio

The following functionality was released in September, 2021.

## Use More than One Identity in Your Serverside Campaigns

Now you can use more than one identity attribute in your Serverside Event API
requests to get more flexibility when you configure Serverside campaigns.
Previously, you configured requests to include one identity attribute for
lookup and merge.

Why: Any identity attributes that you now provide in the request are used in
lookup and merge. And you aren’t required to pass a default identity as user
ID in the Serverside Event API. Instead, you can pass identities as user
attributes to Interaction Studio.

Where: This change applies to Premium Edition.

## Gain More Flexibility in Identity Setup with Profile ID

The Interaction Studio Multiple Identity System now has another built-in
identity for export or merge. Profile ID is the new system-generated ID for
each unique and known customer profile that gives you more flexibility when
you set up your identity system.

Where: This change applies to Premium Edition.

## User Profile Objects

You can now extend profile data storage by configuring Profile Objects
containing user-specific or business-related catalog information. User Profile
Objects increase customer access to existing data storage mechanisms for user
profiles and provide a rules framework to help you use this data for
segmentation and campaign targeting.

Why: Profile Objects eliminate the distinction between Item Types and
Dimensions. And Catalog Objects now avoid the mistaken assumption that there’s
a parent and child relationship between items and dimensions.

Who: To use this feature, you must have Configure Catalog and Profile Objects
permissions.

User Profile Objects (New Feature): | Catalog Objects (Updates or Existing Catalog System):  
---|---  
New Object type for Users “User Profile Objects” New Enhancements to Catalog Objects New Profile Object tab on the user profile New User Profile Object ETL New User Profile Object rules for segmentation and campaign targeting  |  Catalog Set-Up screen moving to Settings > Catalog and Profile Objects Removing separation of Item Types and Dimensions to be simply “Catalog Objects” All catalog items on the catalog and profile object set-up screen will be grouped under Catalog Objects Concept of “Dimensions” changing to “Related Catalog Objects” All ETLs and sitemaps that use Dimensions will continue to function (update is backwards compatible) Dimension ETL being deprecated and replaced with Catalog Object ETL Any existing dimension ETL’s that are running will continue to function Cardinality now defined at the relationship level instead of at the object level 

