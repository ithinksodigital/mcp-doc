

# Connect the Personalization SFTP to Marketing Cloud for ETL Data Feeds

In Automation Studio, configure a process to automatically send CSV export
files from Marketing Cloud Engagement data extensions to Marketing Cloud
Personalization.

### Required User Permissions

Permissions Needed  
---  
To connect to Marketing Cloud: | A role with Administrator permissions  
  
  1. If you don’t already have an SFTP account, see [Create an SFTP Account](https://help.salesforce.com/s/articleView?id=sf.mc_pers_sftp_account_create.htm&language=en_US&type=5 "Send and receive data from an automated platform safely and securely using ETL Integration. After you create an SFTP account, add the credentials to your FTP client.").
  2. In Marketing Cloud Engagement, hover over your name and click **Setup**.
  3. From the **Administration** section of the main navigation, select **Data Management** | **File Locations**.
  4. Click **Create**.
  5. Enter the properties for the file location:

Property | Description  
---|---  
**Name** | Enter a name that includes the dataset and folder, such as Personalization Production Inbound.  
**External Key** | Leave this field blank.  
**Description** | Enter a description of the file location related to the dataset and folder.  
  
  6. Select **External SFTP Site** from the **Location Type** dropdown and complete the following fields:

Field | Description  
---|---  
**URL** | Enter the SFTP URL in the following format: `FTP_DOMAIN_NAME/DATSET_NAME/inbound`, such as `sftp.germany-2.evergage.com/engage/inbound`.  
**FTP_DOMAIN_NAME** | Enter the host name of your Personalization SFTP server, such as `sftp.germany-2.evergage.com`. It appears in the last column of the SFTP user credentials CSV file.  
**DATASET_NAME** | Enter the ID of the Personalization dataset that contains the segment you’re exporting, such as `engage`.  
**Port** | Enter `22`.  
**Username** | Copy and paste the SFTP username from the CSV file you downloaded when you created the SFTP account.  
**Auth Type** | Select **Password** from the dropdown.  
**Password** | Copy and paste the SFTP password from the CSV file you downloaded when you created the SFTP account.  
**Retype Password** | Copy and paste the SFTP password from the CSV file you downloaded when you created the SFTP account.  
  
  7. Click **Save**.
  8. Repeat this process for each dataset you have, such as Test Inbound and Production Inbound.

Next

**[Create a Source Data Extension in Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_source_data_extension.htm&language=en_US&type=5
"In Automation Studio, configure a process to automatically load CSV export
files from Marketing Cloud Engagement data extensions into Marketing Cloud
Personalization using ETL data feeds.")**

