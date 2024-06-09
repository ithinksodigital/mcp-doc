

# User ETL Data Feed

Use the User ETL data feed to update Unified Custom Profiles, and Unified
Account Profiles if you have B2B Detect. Personalization stores user profiles
for each anonymous and known user in the system.

## About Ingesting User Data

User ETL data feeds are unique in that Personalization often receives user
data from multiple sources that are all canonical. For this reason, a blank
value in the User ETL file doesn’t impact the existing value like it does in
other ETL files.

The User ETL data feed also supports updating any user profile attributes
you’ve created.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with `attribute:` must match the custom attribute names on the User Attributes tab of the Settings > Attributes page. 

## Filename Format

`user-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`userId` or an identity attribute | Required. Only unique identities can be included and updated through an ETL feed. This field has a four-character minimum requirement.If you aren’t using Personalization's multiple identities system, a user ID must be included. This ID must be one that is tracked within the system so that the events can be tied to the specific user profile.If you're using Personalization's multiple identities system, `userId` isn’t referenced in ETL files. At least one identity attribute is required. Multiple identity attributes can be included for a single user by including multiple columns in the file. There is a limit of five identity attributes for the User ETL.The correct header format for identity attributes is `attribute:` followed by the name of the identity attribute name as it appears in Personalization. | jdoejohn.doe@example.com C2e384084c8ac233attribute:emailAddressattribute:sfmcContactKeyattribute:customerIdattribute:sfcrmContactIdattribute:sfcrmLeadId | 120 | String  
`attribute:` | The custom attributes for the user. Column headers begin with `attribute:` and are followed by the attribute name as it appears on the Attributes page. The header value must match the attribute name in the system, and the values must conform to the configured data type. | attribute:isLoggedIntrueattribute:userLevel5 | 1024 | Any valid data type  
`attribute:name` | The display name for the user. | Santa ClausEaster Bunny | 120 | String  
`attribute:accountId` | Represents the unique identifier for an account, and its value must match an account ID in the system. Account IDs must be all lowercase with no spaces.Note: This field is available only if you have B2B Detect enabled. | salesforce 6413150145 | 120 | String  
  
## Sample File Structure: Not using the multiple identities system

userId  | attribute:name  | attribute:emailAddress  | attribute:accountId  | attribute:isLoggedIn  | attribute:visitNumber  | attribute:firstVisitDate   
---|---|---|---|---|---|---  
jdoe | John Doe | johndoe@example.com |  | TRUE | 40 | 2017-07-17  
tester@test.com | Tester | tester@test.com | testaccount | TRUE | 15 | 2009-10-19T08:42:58Z  
user103925 |  |  |  | FALSE | 1 | 2020-07-07  
a30bkcqfo941afc | Jane Smith | example@example.com | example | TRUE | 3 | 2020-04-01  
personalizationuser | Personalization User | testing@test.com | personalization | TRUE | 6130 | 2010-01-01  
  
## Sample File Structure: Using the multiple identities system

attribute:emailAddress  | attribute:customerId  | attribute:name  | attribute:accountId  | attribute:isLoggedIn  | attribute:visitNumber  | attribute:firstVisitDate   
---|---|---|---|---|---|---  
johndoe@example.com | 3910vi2msp38g4 | John Doe |  | TRUE | 40 | 2017-07-17  
tester@test.com | 8491505268e12f | Tester | testaccount | TRUE | 15 | 2009-10-19T08:42:58Z  
| 8f138t9fd128d1v |  |  | FALSE | 1 | 2020-07-07  
example@example.com | 19218sdfee31sav | Jane Smith | example | TRUE | 3 | 2020-04-01  
testing@test.com | 9851ar4vbt450em | Personalization User | personalization | TRUE | 6130 | 2010-01-01  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")
  * [ETL Ingestion Performance](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_performance.htm&language=en_US&type=5 "Marketing Cloud Personalization doesn’t guarantee a throughput rate for ETL ingestion, so it’s helpful to know which factors can affect ETL ingestion rates. Many of these factors depend on the type of record that the feed modifies. ETL processing speeds vary across accounts and datasets.")

