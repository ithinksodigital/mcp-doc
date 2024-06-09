

# Define a Personalization ETL Data Feed Automation

In Automation Studio, configure an automation process to load CSV export files
from Marketing Cloud Engagement data extensions to Personalization, and encode
them using UTF-8.

### Required User Permissions

Permissions Needed  
---  
To define an automation: | A role with Administrator permissions  
  
![9c977699-8e6d-4cba-92f1-779e26237ed2]

Note Personalization requires all CSV feeds to be encoded with UTF-8.
Marketing Cloud Engagement data extension extracts use a different encoding.
If the File Convert data extract type isn’t available, create a support
request to enable it on your account.

To create the automation:

  1. From the main navigation in Marketing Cloud Engagement, select **Journey Builder** | **Automation Studio**.
  2. Click **New Automation**.
  3. Drag **Schedule** from the **Starting Sources** section to the **Start with a Starting Source** dotted circle.
  4. Click **Configure**.
  5. Enter a **Start Date** and **Time** that occurs after the date you expect to finish end-to-end testing of this process.
  6. Confirm the correct **Time Zone**.
  7. Select **Repeat as Daily every 1 day(s)**.
  8. Set the **End** value to a number of occurrences, a specific date, or **never**.
  9. Click **Done**.
  10. Configure the SQL Query activity to load data for the source data extension.
    1. Click **Choose**.
    2. Select the SQL Query Activity you created previously.
  11. Configure a new data extract activity to extract data from a data extension to a CSV file.
    1. Click **Choose**.
    2. Click **Create New Data Extract Activity**.
    3. For Extract Type, select **Data Extension Extract**.
    4. Define a filename pattern.

This field depends on the Extract, Transform, Load (ETL) data feed type. See
the ETL file requirements for the ETL data type.

    5. For **Column Delimiter** , select the comma (,).
    6. For **DECustomer Key** , enter the customer key for your source data extension.
    7. Select the **Has Column Headers** and **Text Qualified** options.
  12. Configure a new data extract activity to convert .csv files to UTF-8.
    1. Click **Choose**.
    2. Click **Create New Data Extract Activity**.
    3. For **Extract Type** , select **File Convert**.
    4. Define a filename pattern.

This field depends on the ETL data feed type. See the ETL file requirements
for the ETL data type.

    5. For **Convert To** , select **UTF8**.
    6. Select the **Is File In Safe House** option.
  13. Configure a new file transfer activity to transfer CSV files to the Personalization SFTP.
    1. Click **Choose**.
    2. Click **Create New File Transfer Activity**.
    3. Select **Move a File From Safehouse**.
    4. Define a filename pattern.

This field depends on the ETL data feed type. See the ETL file requirements
for the ETL data type.

    5. For **Destination** , select **Interaction Studio SFTP**.
  14. Add and configure more activities as necessary.
  15. Save your work.
  16. To test the automation, ensure that a file resides in the inbound SFTP folder. Click **Run Once**. New records appear on the target data extension. When testing is complete, activate the automation by clicking **Active** and then **Activate**.

Previous

**[Load Data to a Source Data
Extension](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_source_data_extension_load.htm&language=en_US&type=5
"Use a SQL query to retrieve data from other data extensions and standard
views of Marketing Cloud Engagement, transform the data to the required
format, and save it to the source data extension.")**

