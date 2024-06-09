

# Create a Source Data Extension in Marketing Cloud

In Automation Studio, configure a process to automatically load CSV export
files from Marketing Cloud Engagement data extensions into Marketing Cloud
Personalization using ETL data feeds.

### Required User Permissions

Permissions Needed  
---  
To create a target data extension: | A role with Administrator permissions  
  
  1. From the main navigation in Marketing Cloud Engagement, select **Audience Builder** | **Contact Builder**.
  2. Click **Data Extensions**.
  3. Click **Create**.
  4. Complete the values in the **Properties** section.

Value | Setting  
---|---  
Creation Method | **Create from New**  
Name | Enter a descriptive name for the segment. To more easily identify the data extension in Contact Builder, we recommend using a name that matches the segment.  
Description | Enter a description so you can more easily identify the data extension in Contact Builder.  
Is Sendable | Select to make the data extension available as the send source.  
Is Testable | Select to make the data extension available for testing.  
  
  5. Click **Next**.
  6. For **Data Retention** , click **On** to set a data retention policy for the data extension. 
  7. To apply the data retention policy to any entities, select the **Apply To** option for them.
  8. Define how long you want to retain data in the **Retention Period** section. For example, enter “6” in the number field and select “Months” as the time frame to enforce a six-month data retention policy.
  9. Click **Next**.
  10. Configure the columns you want to load. 

![f2233760-bd3a-4804-b419-40b34a9c7553]

Note Column names must match field names specified in the ETL file
requirements. Attributes must exist in the Personalization system and must be
prepended with `attribute:`. To learn more, see [Available ETL Data
Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5
"Use these ETL data feeds for ETL integration.").

The following example shows configuring an ETL data feed for user or
subscriber data (see [User ETL Data
Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5
"Use the User ETL data feed to update Unified Custom Profiles, and Unified
Account Profiles if you have B2B Detect. Personalization stores user profiles
for each anonymous and known user in the system.")). The first column is
required, maps to an identity attribute, and is configured as the primary key.
The remaining columns are mapped to other user attributes.

![d8a29e3e-742d-4f59-906b-2b90ecbbf1be]

Note When defining data extension fields, don’t specify a value of `Date` for
any attribute data types.

Column Name | Settings  
---|---  
`attribute:sfmcContactKey` | 
     * **Name:** attribute:sfmcContactKey
     * **Data Type:** Text
     * **Length:** 50
     * **Primary Key:** Selected
     * **Nullable:** Not selected  
`attribute:name` | 
     * **Name:** attribute:name
     * **Data Type:** Text
     * **Length:** 50
     * **Primary Key:** Not Selected
     * **Nullable:** Selected  
`attribute:isLoggedIn` | 
     * **Name:** attribute:isLoggedIn
     * **Data Type:** Text
     * **Length:** 50
     * **Primary Key:** Not Selected
     * **Nullable:** Selected  
`attribute:firstVisitDate` | 
     * **Name:** attribute:firstVisitDate
     * **Data Type:** Text
     * **Length:** 50
     * **Primary Key:** Not Selected
     * **Nullable:** Selected  
  
  11. Click **Create** and then **OK**.
  12. Open the data extension and save the External Key. You need the external key when you set up data extracts in Automation Studio.

Previous

**[Connect the Personalization SFTP to Marketing Cloud for ETL Data
Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_connect_sftp.htm&language=en_US&type=5
"In Automation Studio, configure a process to automatically send CSV export
files from Marketing Cloud Engagement data extensions to Marketing Cloud
Personalization.")**

Next

**[Load Data to a Source Data
Extension](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_source_data_extension_load.htm&language=en_US&type=5
"Use a SQL query to retrieve data from other data extensions and standard
views of Marketing Cloud Engagement, transform the data to the required
format, and save it to the source data extension.")**

