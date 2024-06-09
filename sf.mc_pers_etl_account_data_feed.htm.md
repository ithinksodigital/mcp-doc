

# Account ETL Data Feed

Use the Account ETL data feed to update account information in Unified Account
Profiles.

## About Ingesting Account Data

If you market to businesses, you can use Unified Account Profiles to display
aggregate information that Personalization collects about a particular
account. Unified Account Profiles provide a comprehensive view of each of your
accounts according to the cross-channel interactions of customers and
prospects.

The accounts can be linked with firmographic data to gain more information.
Any previously known information about the accounts can be loaded into the
system by creating attributes to reflect the keys in the source system. Custom
attributes can also be defined.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with `attribute:` must match the custom attribute names on the Account Attributes tab of the Settings > Attributes page. 

## Filename Format

`account-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`accountId` | Represents the unique identifier for an account, and its value must match an account ID in the system. Account IDs must be all lowercase with no spaces. | salesforce 6413150145 | 120 | String  
`attribute:name` | The display name for an account. | SalesforceExample Company | 120 | String  
`attribute:` | The custom attributes for the account. Column headers begin with `attribute:` and are followed by the attribute name as it appears on the Attributes page. The header value must match the attribute name in the system, and the values must conform to the configured data type. | attribute:numEmployees1250attribute:companySizemediumattribute:inBusinessFlagtrue | 1023 | Any valid system data type  
  
## Sample File

accountId  | attribute:name  | attribute:numEmployees | attribute:companySize | attribute:inBusinessFlag  
---|---|---|---|---  
6413150145 | Example Company | 1268 | medium | TRUE  
8418416741 | Sample Company | 7358 | medium | True  
9177215300 | Obsolete Company | 21 | small | false  
salesforce | Salesforce | 56,606 | large | true  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

