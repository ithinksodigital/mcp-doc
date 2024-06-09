

# About User Profile Objects

Learn more about user profile objects.

The behavioral data that Personalization collects about your users is in the
context of the catalog that you configure. So the more detailed your catalog,
the more granular your insight into customer engagement and affinities. User
profile objects contain user-specific information that you can use to describe
a user's relationship to a catalog object. You can also associate attributes
with user profile objects.

User profile objects can be powerful tools for cross-channel campaign
targeting. Before you create user profile objects, decide what type of data
you want to track. Examples of user profile objects are: vehicle lease, home
mortgage, credit card ownership, banking accounts, subscriptions, loans,
mortgages, product registrations, service cases, and event attendance.

## User Profile Object Attributes

User profile object attributes provide metadata that Personalization uses when
managing data. Examples of attributes include ID, name, URL, dates, inventory,
price, currency, and rating. You can reference user profile object attributes
in segmentation and web campaign rules.

## Related Catalog Objects

You can associate related catalog objects with a user profile object to
provide more in-depth descriptions of your catalog items. You can reference
the related catalog objects in segmentation and web campaign rules.

## Managing User Profile Objects

A green check mark beside a user profile object’s name indicates that it’s
enabled, visible within your catalog, and available to use.

If you’re editing a user profile object with a green check mark, any changes
you make to attributes or related catalog objects can impact what
Personalization stores for that user profile object. If you change these
values and are capturing catalog data using the sitemap or an ETL, make sure
that you also change the sitemap and ETL file schema. Otherwise,
Personalization can’t store the data you send because it no longer matches the
user profile object definition.

If you’re planning to edit or disable a user profile object, be sure to consider the impact that can have on any related catalog objects or related user profile objects that you’ve associated with it. You can check for associations by selecting **Settings** | **Catalog and Profile Objects** and selecting the desired user profile object. The associations appear at the upper right in the Current Relationships section.

When you delete a user profile object, you can no longer reference it using
campaign and segment rules. In addition, the profile object is no longer
associated with any related catalog objects or related user profile objects.
However, those references and associations remain in Personalization
historical data. If you recreate a deleted profile object using the same name,
the references and associations return.

#### See Also

  * [Create a User Profile Object](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_create.htm&language=en_US&type=5 "Create user profile objects and their relationships to better define your Personalization users. Once created, you can use these objects in segmentation and campaign targeting to improve cross-channel personalization. You update, add, and remove user profile object data profile with the User Profile Object ETL.")
  * [User Profile Object Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_rule.htm&language=en_US&type=5 "Use built-in user profile object rules to help improve cross-channel personalization in segmentation and web campaign targeting. User profile objects have two built-in rules—object aggregation and object match.")
  * [User Profile Object Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_limits.htm&language=en_US&type=5 "Marketing Cloud Personalization imposes limits per dataset for user profile objects.")

