

# Load Data to a Source Data Extension

Use a SQL query to retrieve data from other data extensions and standard views
of Marketing Cloud Engagement, transform the data to the required format, and
save it to the source data extension.

### Required User Permissions

Permissions Needed  
---  
To load data to a source data extension: | A role with Administrator permissions  
  
The following steps describe the process using a SQL query, but you can use
another method.

  1. From the main navigation in Marketing Cloud Engagement, select **Journey Builder** | **Automation Studio**.
  2. Click the **Activities** tab.
  3. Click **Create Activity**.
  4. Prepare your SQL Query Activity similar to the SQL Query Example in the Examples section.
  5. **Extract date fields:** Format dates in the ISO 8601 format, such as the format function: `FORMAT(YOUR_DATE_COLUMN, 'yyyy-MM-ddTHH:mm:ssZ')`

Timezone offsets aren’t supported.

  6. **Extract Boolean fields:** Use “TRUE” or “FALSE” for boolean values. By default, Marketing Cloud Engagement exports boolean values as “1” or “0”. To convert a Boolean value to the right format use: `IIF(YOUR_BOOLEAN_COLUMN = 1, 'TRUE', 'FALSE')`
  7. Continue configuring the SQL Query Activity. Select your source data extension and use the **Overwrite** method for faster processing.
  8. To ensure that everything works as expected and the query populates your source data extension, manually run your SQL query.
  9. To complete the integration process, perform the steps in [Define a Personalization ETL Data Feed Automation](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_load_automated.htm&language=en_US&type=5 "In Automation Studio, configure an automation process to load CSV export files from Marketing Cloud Engagement data extensions to Personalization, and encode them using UTF-8.").

![d8a63411-6aec-42a6-8815-85d098d29198]

Example

**SQL Query Example**

    
    
    select
    Lower(SubscriberKey) as "attribute:sfmcContactKey",
    FirstName as "attribute:name",
    Email_Address as "attribute:emailAddress",
    Number_Of_Visits as "attribute:visitNumber",
    
    IIF(Known_Subscriber = 1, 'TRUE', 'FALSE') as "attribute:isLoggedIn",
    FORMAT(Registration_Date, 'yyyy-MM-ddTHH:mm:ssZ') as "attribute:firstVisitDate"
    from
    ContactMaster
    

Previous

**[Create a Source Data Extension in Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_source_data_extension.htm&language=en_US&type=5
"In Automation Studio, configure a process to automatically load CSV export
files from Marketing Cloud Engagement data extensions into Marketing Cloud
Personalization using ETL data feeds.")**

Next

**[Define a Personalization ETL Data Feed
Automation](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_load_automated.htm&language=en_US&type=5
"In Automation Studio, configure an automation process to load CSV export
files from Marketing Cloud Engagement data extensions to Personalization, and
encode them using UTF-8.")**

