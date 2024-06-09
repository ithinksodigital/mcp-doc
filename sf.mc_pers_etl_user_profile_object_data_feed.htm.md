

# User Profile Object ETL Data Feed

Use the User Profile Object ETL data feed to update the user profile objects
you create.

## About Ingesting User Profile Object Data

When merging user profiles, Personalization appends all user profile objects
to the new, combined user profile. If the resulting number of user profile
objects for an object type exceeds the limit of 100, Personalization retains
the 100 most recent based on their creation date.

A shared object ID doesn’t cause user profiles to merge. When Personalization
merges user profiles that share an object ID, it retains the most recently
created user profile object and its metadata.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Before uploading a user profile object ETL data feed, confirm that the user profile object is configured and enabled on the Catalog and Profile Objects page. Also, be sure to add any applicable related catalog objects and attributes to the user profile object. 

![a37ebfb6-1e21-4cfd-86cb-187372062b45]

Note If the ETL file includes data for a user profile object, related catalog
object, or attribute that isn’t configured, Personalization doesn’t apply that
data. Configure user profile objects, related catalog objects, and attributes
before uploading the ETL file.

  * Review the [User Profile Object Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_limits.htm&language=en_US&type=5 "Marketing Cloud Personalization imposes limits per dataset for user profile objects.") before uploading any user profile object data.
  * If an ETL data feed causes a user profile to exceed 100 user profile objects of a certain type, Personalization keeps the 100 most recent objects.
  * The user profile object ETL file has a unique column header format for identity attributes. Instead of using `attribute:` as in other ETL files, you use `identityAttribute:`.
  * User profile object ETL files must be sorted by identity before uploading them so that all objects associated with a user are grouped. If you’re not using the multiple identities system, sort the file by userId. If you’re using the multiple identities system: 
    * Sort the file so that all objects for each user are grouped.
    * If multiple identity attribute columns are present in the file and a user appears on multiple rows, the same identity values must be present for each of those rows. For example, If you’re uploading a lease profile object file and a single user has multiple lease objects, each row must contain the same identity attribute values for that user. So, if there are four identity attribute columns in the file, and the user has values for three of them, those three values must be present in each row for that user. If the identity values aren’t consistent across rows for a user, data can be overwritten, misapplied, or ignored.
  * Each user profile object ETL file can only reference a single object type. The object type is defined in the filename and must map to the user profile object name on the Catalog and Profile Objects page. So, if you have four user profile objects configured on the Catalog and Profile Objects page, and you want to upload data for each, you need one file for each object type.
  * Include information in all columns for a user profile object, even if the data isn’t changing. If you leave a column empty, Personalization clears the existing value for the user profile object. To retain an existing value, you must include it in the file.
  * The object type ID and file mode are critical to how Personalization processes the information in the file. 
  * The file number at the end of the filename helps you track user profile object updates. It doesn’t impact how the file runs or processes.
  * Field names that begin with `attribute:` must match the custom attribute names in the Attributes section of the Catalog and Profile Objects page for that user profile object. Field names that begin with `identityAttribute:` must match the custom attribute names on the Settings > Identity Types page. 

## Delta and Replace Modes

The user profile object ETL file has two modes: delta and replace. The file
mode is defined in the filename.

Mode | Description  
---|---  
Delta mode | 

  * Personalization only updates the user profile objects in the file. If a user profile object isn’t included in the file, it remains unchanged.
  * The delta mode is the only mode that supports the "remove" column header. Remove deletes the specified user profile object for the user.

  
Replace mode | 

  * Personalization replaces all user profile objects for the object type for that user.
  * If an object ID for an existing user profile object isn’t included in the file, Personalization deletes it from the user profile.

  
  
## Filename format

`user-profile-objects-<objectTypeId>-<delta/replace>-<file number>.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`userId` or an identity attribute | Required. Only unique identities can be included and updated through an ETL feed. This field has a four-character minimum requirement.If you aren’t using Personalization's multiple identities system, a user ID must be included. This ID must be one that is tracked within the system so that the events can be tied to the specific user profile.If you're using Personalization's multiple identities system, `userId` isn’t referenced in ETL files. At least one identity attribute is required. Multiple identity attributes can be included for a single user by including multiple columns in the file. There is a limit of five identity attributes for the User Profile Object ETL.The correct header format for identity attributes is `identityAttribute:` followed by the name of the identity attribute name as it appears in Personalization. | jdoe john.doe@example.com C2e384084c8ac233identityAttribute:emailAddressidentityAttribute:sfmcContactKeyidentityAttribute:customerIdidentityAttribute:sfcrmContactIdidentityAttribute:sfcrmLeadId | 120 | String  
`objectId` | Each object for a user requires an object ID, which Personalization uses for updates and replacements. The `objectId` is different from the ObjectTypeId that appears in the filename. The ObjectTypeId maps to the name of an object type configured on the Catalog and Profile Objects page. This object ID is the unique identifier for a user profile object stored on a user profile.An object ID must be alphanumeric and contain only letters, numbers, dashes, and underscores. An object ID can exist across multiple users. | mortgage1lease1case123 | 30 | String  
`attribute:<attribute name>` | The custom attributes for the user profile object. The attribute must be preconfigured on the Catalog and Profile Objects page. The ETL data feed can’t create an attribute for a user profile object.Column headers begin with `attribute:` and are followed by the attribute name as it appears in the Attributes section of the Catalog and Profile Objects page for the user profile object. The header value must match the attribute name in the system, and the values must conform to the configured data type.If you leave an attribute column empty, Personalization clears the existing value for the object. To retain an existing value, you must include it in the file, even if it isn’t changing. | String:

  * `attribute:loyaltyTier`
  * `attribute:subscriberEmail`

Integer/Decimal:

  * `attribute:APR`
  * `attribute:caseTier`

Boolean:

  * `attribute:caseOpen`
  * `attribute:active`

Date:

  * `attribute:leaseStart`
  * `attribute:endDate`

The format is an [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date/time string. Timezone offsets aren’t supported. | Dependent upon data type | String, decimal, Boolean, integer, date  
`relatedCatalogObject:<catalog object name>` | The related catalog objects configured for the user profile object. The related catalog object must be assigned to the user profile object on the Catalog and Profile Objects page. If a related catalog object in the file isn’t assigned to the user profile object, Personalization ignores it. Column headers begin with “relatedCatalogObject:” and are followed by the catalog object name. If the cardinality of the related catalog object is “many per item,” separate the values using the pipe (|) symbol. | Mortgage Example:Product: creditCard|debitCardMortgageType: fixedRateMortgageCar Lease Example:CarMake: carMake1CarModel: carModel1 | 255 | String  
`remove` | To delete a user profile object from a user profile, include the column header "remove" and set the value as true. If the "remove" header is present and it’s blank, the default value is false. You can’t recover a user profile object after it’s deleted.  | TRUEtrue | 1023 | String  
  
## Sample File Structure: Not using the multiple identities system

user-profile-objects-Lease-delta-1.csv

userId  | objectId  | attribute:startDate  | attribute:endDate  | attribute:Mileage  | attribute:active  | relatedCatalogObject:Make  | relatedCatalogObject:Model  | relatedCatalogObject:Year  | remove   
---|---|---|---|---|---|---|---|---|---  
jdoe123 | lease1 | 2022-01-01T00:00:00.000Z | 2024-01-01T00:00:00.000Z | 30000 | TRUE | Jeep | Wrangler | 2022 |   
jdoe123 | lease2 | 2022-01-01T00:00:00.000Z | 2024-01-01T00:00:00.000Z | 50000 | TRUE | Jeep | Grand Cherokee | 2022 |   
user103925 | lease3 | 2022-01-01T00:00:00.000Z | 2026-01-01T00:00:00.000Z | 75000 | TRUE | Chrysler | Pacifica | 2022 |   
a30bkcqfo941afc | lease4 | 2022-01-01T00:00:00.000Z | 2026-01-01T00:00:00.000Z | 50000 | TRUE | Ford | Ranger | 2022 |   
personalizationuser | lease5 |  |  |  |  |  |  |  | TRUE  
  
## Sample File Structure: Using the multiple identities system

user-profile-objects-Mortgage-delta-1.csv

userId  | objectId  | attribute:startDate  | attribute:endDate  | attribute:APR  | attribute:active  | relatedCatalogObject:Mortgage  | relatedCatalogObject:Product  | remove   
---|---|---|---|---|---|---|---|---  
jdoe123 | mortgage1 | 2022-01-01T00:00:00.000Z | 2024-01-01T00:00:00.000Z | 0.4 | TRUE | fixedRateMortgage | debitCard |   
jdoe123 | mortgage2 | 2022-01-01T00:00:00.000Z | 2024-01-01T00:00:00.000Z | 0.25 | TRUE | adjustableRateMortgage | creditCard |   
user103925 | mortgage3 | 2022-01-01T00:00:00.000Z | 2026-01-01T00:00:00.000Z | 0.3 | TRUE | conventionalLoan | creditCard |   
a30bkcqfo941afc | mortgage4 | 2022-01-01T00:00:00.000Z | 2026-01-01T00:00:00.000Z | 0.35 | TRUE | fixedRateMortgage | debitCard |   
personalizationuser | mortgage5 |  |  |  |  |  |  | TRUE  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

