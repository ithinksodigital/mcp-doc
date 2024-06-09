

# External Email Campaign Events ETL Data Feed

You can use the External Email Campaign Events ETL data feed to import data
from email campaigns that were sent by an external email service provider
(ESP). Data can include sends, opens, and clicks.

## About Ingesting External Email Campaign Events Data

Personalization stores the data that you include in an External Email Campaign
Events ETL file in a third-party campaign object for the user profile. This
data is subsequently available for segmentation and targeting purposes.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with `attribute:` must match the custom attribute names on the User Attributes tab of the Settings > Attributes page. 

## Filename Format

`externalEmailCampaign-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`userId` or an identity attribute | Required. Only unique identities can be included and updated through an ETL feed.If you aren’t using Personalization's multiple identities system, a user ID must be included. This ID must be one that is tracked within the system so that the events can be tied to the specific user profile.If you're using Personalization's multiple identities system, userId isn’t referenced in ETL files. At least one identity attribute is required. Multiple identity attributes can be included for a single user by including multiple columns in the file. The correct header format for identity attributes is `attribute:` followed by the name of the identity attribute name as it appears in Personalization. | user@example.comattribute:emailAddressattribute:sfmcContactKeyattribute:customerIdattribute:sfcrmContactIdattribute:sfcrmLeadId | 120 | String  
`externalCampaignId` | Required. The unique identifier for the external campaign. | 3823923QLcjsAjC | 1023 | Any  
`externalCampaignName` | The unique name for the campaign. | Example_campaignnameTestcampaign_242424testcampaign | 1023 | String  
`eventType` | Required. The type of event, such as send, click, open. | SendClickOpen | 120 | String  
`eventDate` | Required. The date and time that the event occurred. | 2017-04-22T10:23:3 7Z | 1023 | Date  
`externalSystem` | Required. The system that ran the campaign. | Salesforce Marketing CloudEloquaMarketoResponsys | 1023 | String  
`source` |  Represents the source of the campaign. Data ingested for this attribute are not available for use in segmentation or targeting. |  | 1023 | String  
`medium` |  Represents the medium of the campaign. Data ingested for this attribute are not available for use in segmentation or targeting. |  | 1023 | String  
  
## Sample File Structure: Not using the multiple identities system

userId  | externalCampaignId  | externalCampaignName  | eventType  | externalSystem  | eventDate   
---|---|---|---|---|---  
jdoe | 3823923 |  | Send | Salesforce Marketing Cloud | 2022-07-17T11:24:23Z  
tester@test.com | QLcjsAjC |  | Open | Eloqua | 2021-10-19T08:42:58Z  
user103925 | newsletterCampaign | Newsletter Campaign | Click | Responsys | 2022-07-07T10:11:34Z  
  
## Sample File Structure: Using the multiple identities system

attribute:emailAddress  | attribute:customerId  | externalCampaignId  | externalCampaignName  | eventType  | externalSystem  | eventDate   
---|---|---|---|---|---|---  
jdoe@ac.com | 123456 | 3823923 |  | Send | Salesforce Marketing Cloud | 2022-07-17T11:24:23Z  
tester@test.com | 111234 | QLcjsAjC |  | Open | Eloqua | 2021-10-19T08:42:58Z  
bob@test.com | 675908 | newsletterCampaign | Newsletter Campaign | Click | Responsys | 2022-07-07T10:11:34Z  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

