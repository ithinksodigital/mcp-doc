

# Create a Target Data Extension in Marketing Cloud

Set up a target data extension in Marketing Cloud to map the fields in the
segment that you’re exporting. After you create the data extension, save the
external key to set up data extracts in Automation Studio.

### Required User Permissions

Permissions Needed  
---  
To create a target data extension: | A role with Administrator permissions  
  
  1. From the main navigation in Marketing Cloud, select **Audience Builder** | **Contact Builder**.
  2. Click **Data Extensions**.
  3. Click **Create**.
  4. Complete the information in the Properties section.

Item | Description  
---|---  
**Creation Method** | Select **Create from New**.  
**Name** | Enter a name that matches the segment so that you can identify the data extension in Contact Builder.  
**Description** | Enter a description to identify the data extension.  
**Is Sendable** | Makes the data extension available as the source of a send.  
**Is Testable** | Makes the data extension available for testing.  
  
  5. Click **Next**.
  6. To set a data retention policy for your data extension, turn on Data Retention. 
  7. To apply the data retention policy, select **Apply To**.
  8. Configure an option for the Retention Period. For a revolving time period, enter a value in the text field and select a time frame from the dropdown. For a fixed date, select the date.
  9. Click **Next**.
  10. Configure the mandatory attributes.

Attribute names in the segment that you’re exporting must match field names in
the data extension. When you begin entering column values in a row, an empty
row is added to receive the next group of attributes.

![22d9ee7d-641e-47ae-8c09-5b2b3a728050]

Note If the Personalization system populates the sfmcContactKey attribute, map
SubscriberKey to sfmcContactKey.

Primary Key | Name | Data Type | Required (is this “Nullable”?) | Length | Default Value  
---|---|---|---|---|---  
Selected | userId | Text | Not selected | 50 | N/A  
Not selected | segmentMembership | Boolean | Selected | Blank | N/A  
Not selected | emailAddress | Email Address | Selected | 254 | N/A  
Not selected | sfmcContactKey | Text | Selected | 50 | N/A  
  
  11. Map any other attributes, like country or language using these values:

Primary Key | Name | Data Type | Required (is this “Nullable”?) | Length | Default Value  
---|---|---|---|---|---  
Not selected | <Field name that maps to the attribute> | Text | Not selected | 50 | N/A  
  
  12. Click **Create**.
  13. Click **OK**.
  14. Open the data extension and save the external key. You need the external key when you set up data extracts in Automation Studio.

Previous

**[Connect the Personalization SFTP to Marketing Cloud for Segment
Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_sftp_load_marketing_cloud.htm&language=en_US&type=5
"To receive Personalization segments, configure the Personalization SFTP in
Marketing Cloud. You can create a file location and add your existing SFTP
account details.")**

Next

**[Find a Segment’s
ID](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_id_find.htm&language=en_US&type=5
"You use a segment’s ID when defining its automation process in Automation
Studio. There are also instances when you need a segment’s ID for an ETL data
feed.")**

