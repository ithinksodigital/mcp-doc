

# Manual Segment ETL Data Feed

Use the Manual Segment ETL data feeds to maintain manual segments.

## Create Manual Segments

Before using the Manual Segment ETL data feeds to update manual segments, you
must create those segments in Personalization. The Manual Segment ETL data
feeds can only update existing segments and can’t create additional segments.
These ETL data feeds only add or remove user profiles from the segment, it
doesn’t update any user profile attributes.

## Delta and Replace Modes

Personalization supports the following file modes for manual segments:

Mode | Description  
---|---  
Delta mode | Adds or removes user profiles from manual segments. This mode supports changes to multiple segments in a single ETL file.   
Replace mode | Replaces all user profiles for a single manual segment with the users in the ETL file. This mode only supports a single segment in an ETL file. To update multiple segments using this mode, you need a separate file for each segment.  
  
## Requirements

  * ETL files must be in a .csv file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with “attribute:” must match the custom attribute names on the User Attributes tab of the Settings > Attributes page. 

## Filename Format

The filename format determines whether processing is in delta mode or replace
mode:

Format | Description  
---|---  
Delta format | `segment-delta-YYYY-MM-DD_HH-MM-SS.csv`  
Replace format | `segment-replace-YYYY-MM-DD_HH-MM-SS.csv`  
  
## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`userId` or an identity attribute | Required. Only unique identities can be included and updated through an ETL feed.If you aren’t using Personalization's multiple identities system, a user ID must be included. This ID must be one that is tracked within the system so that the events can be tied to the specific user profile.If you're using Personalization's multiple identities system, userId isn’t referenced in ETL files. At least one identity attribute is required. Multiple identity attributes can be included for a single user by including multiple columns in the file. The correct header format for identity attributes is “attribute:” followed by the name of the identity attribute name as it appears in Personalization. | jdoejohn.doe@example.comC2e384084c8ac233attribute:emailAddressattribute:sfmcContactKeyattribute:customerIdattribute:sfcrmContactIdattribute:sfcrmLeadId | 120 | String  
`segmentId` | Required. The ID of the segment. See [Find a Segment’s ID](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_id_find.htm&language=en_US&type=5 "You use a segment’s ID when defining its automation process in Automation Studio. There are also instances when you need a segment’s ID for an ETL data feed.") for more information. | abcde | 255 | String  
`updateType` | Identifies whether to add or remove the record for the segment. Accepted values are: Add and Remove. Defaults to Add when not specified.Important: This field is used only by the delta mode. | Add | 255 | String  
  
## Sample File Structure: Not using the multiple identities system, delta mode

userId  | segmentId  | updateType   
---|---|---  
user1 | abcde | Remove  
user2 | abcde | Remove  
user3 | abcde | Add  
user444 | fghij | Remove  
user445 | fghij | Add  
  
##  Sample File Structure: Not using the multiple identities system, replace
mode

userId  | segmentId   
---|---  
userA | klmno  
userB | klmno  
userC | klmno  
userD | klmno  
  
##  Sample File Structure: Using the multiple identities system, delta mode

attribute:alternateId  | attribute:emailAddress  | segmentId  | updateType   
---|---|---|---  
fifthuser | user5@user.com | segm1 | Add  
| johndoe@jdoe.com | segm1 | Add  
| janedoe@jdoe.com | segm1 | Remove  
sampleuser |  | segm2 | Add  
exampleuserid | example@example.com | segm3 | Remove  
  
##  Sample File Structure: Using the multiple identities system, replace mode

attribute:emailAddress  | attribute:alternateId  | segmentId   
---|---|---  
johndoe@jdoe.com |  | segm5  
janedoe@jdoe.com |  | segm5  
| sampleuser | segm5  
example@example.com | exampleuserid | segm5  
user5@user.com | fifthuser | segm5  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

