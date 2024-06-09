

# Management of Sensitive User Information

Personalization uses the JavaScript Beacon to collect behavioral information
for users of your digital properties and provide them with personalized
experiences based on those behaviors. The JavaScript Beacon collects the data
through a user’s browser, encrypts it using SSL, and transfers it to the
Personalization servers. Personalization doesn’t store sensitive data, such as
credit card numbers and some personally identifiable information. You can
decide which sensitive data to collect. Personalization stores non-personally
identifiable and nonsensitive data in its cloud service.

## User Roles

Roles are custom and granular in Personalization. There are two built-in roles
that can view sensitive information:

  * Editor with Export

  * Administrator

Administrators are always able to view sensitive information. You can also
create roles with the combination of permissions, granted by dataset, that
meet the needs of your company and security team. Roles with the Audiences >
User/Account Profile > View Sensitive permissions can also view sensitive
information. Roles that can view sensitive information can’t edit attribute
values marked as sensitive in the Attributes section of a Unified Customer
Profile.

For more information about creating user roles and accounts, see [User Role
Permissions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_setup_user_role_permissions.htm&language=en_US&type=5
"You can create roles by combining dataset-specific permissions.").

## User Profile Attributes

User profile attributes can be marked as sensitive so that system users with
roles that can’t view sensitive information see asterisks for sensitive values
on the Unified Customer Profile and segment lists.

If a user profile doesn’t have sensitive attributes, the Unified Customer
Profile doesn’t display the identity attribute label, regardless of the user’s
permissions to view sensitive attribute values.

![31e4d5c6-9e0a-4ba7-b537-8c9a2fea9776]

Note Only attributes marked as “Sensitive” are hidden. Attributes marked as
“Personally Identifiable” aren’t hidden.

If the UserID attribute for your dataset is set as emailAddress and marked as
sensitive:

  * All email addresses in your dataset are considered sensitive.

  * Roles that can’t view sensitive information can’t search for users by email address. Consider giving email campaign testers higher permissions so that they can preview which email content (dynamic content, recommendations, promotions) displays to specific recipients. Lesser permissions can prevent a campaign tester from simulating email content.

If the UserID attribute for your dataset is set as displayName and marked as
sensitive:

  * All usernames in your dataset are considered sensitive.

  * Roles that can’t view sensitive information can’t search for users by username. Consider giving email campaign testers higher permissions so that they can preview which email content (dynamic content, recommendations, promotions) displays to specific recipients. Lesser permissions can prevent a campaign tester from simulating email content.

The UserID attribute can only be marked sensitive by Personalization Support.
Contact Personalization Support for assistance.

For more information about user profile attributes, see [Create a User Profile
Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_attributes_create.htm&language=en_US&type=5
"User profile attributes can collect data you can use in segmentation,
reporting, or with integrated third-party systems. For example, if you create
a form in Personalization, you can assign each field to an existing attribute.
Depending on the configuration of your dataset, the attributes can either
collect the data for reporting, or can write it to a third-party integrated
system.").

## User IDs

  * The user ID attribute isn’t sensitive information. If you set the user ID attribute to use emailAddress or another sensitive attribute, user roles that can’t view sensitive information can view the user ID attribute even though the value is sensitive. If you want to restrict roles that can’t view sensitive information from viewing user IDs, you must contact Personalization Support.

  * Personalization encrypts User IDs that are marked as sensitive and are contained in URLs or API requests.

  * Roles that can’t view sensitive information see asterisks or encrypted user IDs in fields or locations where user IDs display. Roles that can’t view sensitive information can’t search for users by user ID.

  * API tokens aren’t affected by sensitive attribute restrictions. Roles with access to these tokens have permissions that qualify them to view sensitive data. 

