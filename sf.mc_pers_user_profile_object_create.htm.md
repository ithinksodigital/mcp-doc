

# Create a User Profile Object

Create user profile objects and their relationships to better define your
Personalization users. Once created, you can use these objects in segmentation
and campaign targeting to improve cross-channel personalization. You update,
add, and remove user profile object data profile with the User Profile Object
ETL.

### Required User Permissions

Permissions Needed  
---  
To create a user profile object: | A role with Configure permissions  
  
Before you add user profile objects, decide what type of data you want to
track. Examples of user profile objects are: vehicle lease, home mortgage,
credit card ownership, banking accounts, subscriptions, loans, mortgages,
product registrations, service cases, and event attendance.

  1. From the main navigation, select **Settings** | **Catalog and Profile Objects**.
  2. Click the **+** next to **User Profile Object Types**.
  3. Enter a name for the user profile object that is 3–30 characters, all letters, and starts with a capital letter.

![91fa7c9e-8c70-445d-8bed-2c6f5c6bf4d8]

Note Personalization uses the name in the sitemap, and for ETL data storage
and updates. You can’t change the name after you save the user profile object.
User profile objects and catalog objects can’t have the same name.

  4. Enter a **Label**. Label text represents the user profile object in the Personalization application. For example, if the user profile object name is CustomerCreditCard, the label can be Credit Card.

The label is cosmetic. It doesn’t affect data capture or storage.

  5. Enter a **Description** of up to 200 characters. The description to describe the user profile object and its purpose.

![bce24270-a334-4027-b754-9230bb987db8]

Note Personalization replaces any characters beyond 200 with an ellipsis
(...).

  6. To add a custom attribute for the user profile object, in the **Attributes** section, click **New Attribute**.

You can reference user profile object attributes in segmentation and web
campaign rules.

    1. Enter the **Attribute Name**. Use only alphanumeric characters. Spaces and other special characters are not allowed.

Personalization uses the attribute name in the sitemap, and for ETL data
storage and updates.

    2. Enter the **Label**.

The label is cosmetic and represents the attribute in the Personalization
application.

    3. Select the attribute **Type**.
    4. Click the checkmark icon.
  7. To associate an existing catalog object with this user profile object, in the **Related Catalog Objects** section, click **Add Related Catalog Object**.
    1. Select the **Related Catalog Object**.
    2. Select its **Relationship Cardinality**.
    3. Confirm your selections in the **Output/Preview** column.
    4. Click the checkmark icon.
  8. Turn on the **Enabled** option.
  9. Save your work.

After you configure and enable your user profile objects, you upload data for
them using the User Profile Object ETL. You can then use user profile objects
in segmentation and web campaign targeting to help improve cross-channel
personalization. User profile objects appear as one of the detail tabs at the
bottom of a Unified Customer Profile.

![45183e2a-1f1d-437a-bba8-d2a48f8a7843]

Example

**Lease User Profile Object**

For a vehicle lease, you can use profile object attributes to describe the
lease terms that are unique to each user, such as start date, end date, and
mileage. Then you can use related catalog objects, such as make, model, and
year, to describe the lease.

**Product Registration User Profile Object**

For a product registration, you can use profile attributes to describe a
user’s registration date. Then use a related catalog object to assign the
product ID of the registered item in the catalog listing.

#### See Also

  * [User Profile Object Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_rule.htm&language=en_US&type=5 "Use built-in user profile object rules to help improve cross-channel personalization in segmentation and web campaign targeting. User profile objects have two built-in rules—object aggregation and object match.")
  * [User Profile Object Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_limits.htm&language=en_US&type=5 "Marketing Cloud Personalization imposes limits per dataset for user profile objects.")

