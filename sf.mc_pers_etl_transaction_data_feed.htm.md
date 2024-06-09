

# Transaction ETL Data Feed

Use the Transaction ETL data feed to bulk upload transactions to associate
purchases of items with individual user profiles.

## About Ingesting Transaction Data

This ETL data feed imports transactions into Personalization and associates
them with user profiles by either assigning to an existing user profile or
creating a user profile when there isn’t a matching one.

Each transaction consists of a list of consecutive records for individual line
items that all have the same transactionId. All records of a transaction must
have the same userId and purchaseDate values. Each record in a transaction
must have a productId, price, and quantity.

Sort the file by transaction ID. You can sort the file yourself before
uploading it, or you can enable sorting on the Gear Configuration page by
selecting the Transaction ETL Sort Before Grouping option. If the file isn't
sorted, Personalization doesn’t upload it, so you must sort and resubmit the
file to process it.

When updating a transaction with new information, the entire contents of the
transaction must be present in the file, even if they aren’t changing.
Personalization overwrites any records previously stored for the transaction
if a file contains a transactionId for a previously recorded transaction.
Updates to existing orders do not update statistics derived from the original
order, such as Lifetime Value or daily purchase statistics.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with `attribute:` must match the custom attribute names on the User Attributes tab of the Settings > Attributes page. 

## Filename Format

`transaction-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`userId` or an identity attribute | Required. Only unique identities can be included and updated through an ETL feed.If you aren’t using Personalization's multiple identities system, a user ID must be included. This ID must be one that is tracked within the system so that the events can be tied to the specific user profile.If you're using Personalization's multiple identities system, userId isn’t referenced in ETL files. At least one identity attribute is required. Multiple identity attributes can be included for a single user by including multiple columns in the file. There is a limit of five identity attributes for the Transaction ETL. The correct header format for identity attributes is `attribute:` followed by the name of the identity attribute name as it appears in Personalization. | user168515262jdoe@test.comattribute:emailAddressattribute:sfmcContactKeyattribute:customerIdattribute:sfcrmContactIdattribute:sfcrmLeadId | 120 | String  
`transactionId` | Required. Represents a unique identifier for an individual purchase. All line items from a transaction must have the same transaction ID. | 860340254 | 255 | String  
`purchaseDate` | Required. An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for when the transaction occurred. The first record for a transaction defines the date for the overall order. All dates are stored in UTC time. Timezone offsets aren’t supported. | 2022-04-122022-04-12T11:24:59Z | 1023 | String  
`productId` | Required. Represents the product in your catalog that was purchased in the transaction. If the ID doesn’t match an existing product in your catalog, Personalization creates an item with the productId in the catalog. | prod001 | 255 | String  
`price` | Required. The unit price charged to the user. This field is multiplied by the quantity to determine the total value of this line item. For example, if the price is $1.10 and the quantity is 3, the total value of the line item is $3.30. Use a period as the decimal separator. Don't use thousands separators. | 15063.2510 | 1023 | Decimal  
`quantity` | Required. Represents the net quantity purchased. This field is multiplied by the price to determine the total cost of that line item in the transaction. Then all line items are added to determine the total value of the order. | 150100 | 1023 | Integer  
`attribute:currency` | An [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) currency code of three uppercase letters for the transaction. The currency must be consistent across all records in a transaction. If no currency is provided, the currency defaults to the currency for that dataset.  | USDCADEUR | 3 | String  
`attribute:shipStatus` | Represents the status of the order. Possible values are: shipped, delivered, processing | shippeddeliveredprocessing | 1023 | String  
`attribute:quantityReturned` | Represents the number of items that have been returned. | 025100 | 1023 | String  
  
## Sample File Structure: Not using the multiple identities system

transactionId  | userId  | purchaseDate  | productId  | price  | quantity  | attribute:currency  | attribute:emailAddress  | attribute:shipStatus  | attribute:quantityReturned   
---|---|---|---|---|---|---|---|---|---  
139502841 | user103925 | 2022-04-12 | prod001 | 100.12 | 2 | USD | test@test.com | processing | 0  
139502841 | user103925 | 2022-04-12 | prod001923 | 15.09 | 1 | USD | test@test.com | processing | 0  
139502841 | user103925 | 2022-04-12 | prod005 | 44 | 1 | USD | test@test.com | processing | 0  
492481058 | user049245 | 2022-04-12T10:23:37Z | prod999 | 1.00 | 50 | EUR | user04925@test.com | shipped | 10  
860340254 | user01499 | 2022-01-30 | prod002244 | 15.15 | 3 | AUD |  | delivered |   
860340255 | user2201 | 2022-03-15 | prod1101 | 22.99 | 2 | CAD |  | delivered |   
  
## Sample File Structure: Using the multiple identities system

transactionId  | attribute:emailAddress  | attribute:sfcrmLeadId  | purchaseDate  | productId  | price  | quantity  | attribute:currency  | attribute:shipStatus  | attribute:quantityReturned   
---|---|---|---|---|---|---|---|---|---  
139502841 | test@test.com |  | 2022-04-12 | prod001 | 100.12 | 2 | USD | processing | 0  
139502841 | test@test.com |  | 2022-04-12 | prod001923 | 15.09 | 1 | USD | processing | 0  
139502841 | test@test.com |  | 2022-04-12 | prod005 | 44 | 1 | USD | processing | 0  
492481058 | user04925@test.com | 02941850249856 | 2022-04-12T10:23:37Z | prod999 | 1.00 | 50 | EUR | shipped | 10  
860340254 |  | 561716831115090 | 2022-01-30 | prod002244 | 15.15 | 3 | AUD | delivered |   
860340255 |  | 981361079810570 | 2022-03-15 | prod1101 | 22.99 | 2 | CAD | delivered |   
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

