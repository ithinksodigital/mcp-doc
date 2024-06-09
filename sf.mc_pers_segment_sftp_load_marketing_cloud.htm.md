

# Connect the Personalization SFTP to Marketing Cloud for Segment Exports

To receive Personalization segments, configure the Personalization SFTP in
Marketing Cloud. You can create a file location and add your existing SFTP
account details.

### Required User Permissions

Permissions Needed  
---  
To connect to Marketing Cloud: | A role with Administrator permissions  
  
  1. In Marketing Cloud, hover over your name and click **Setup**.
  2. In the main navigation, under Administration, select **Data Management** | **File Locations**.
  3. Click **Create**.
  4. Enter the properties for the file location.

Property | Description  
---|---  
**Name** | Enter a name that includes the dataset and folder, such as Personalization Production Outbound.  
**External Key** | Leave this field blank.  
**Description** | Enter a description of the file location related to the dataset and folder.  
  
  5. From the Location Type dropdown, select **External SFTP Site** and enter information for these fields.

Field | Description  
---|---  
**URL** | Enter the SFTP URL in the following format: FTP_DOMAIN_NAME/DATSET_NAME/outbound, such as sftp.germany-2.evergage.com/engage/outbound.  
**FTP_DOMAIN_NAME** | Enter the host name of your Personalization SFTP server, such as, sftp.germany-2.evergage.com. It appears in the last column of the SFTP user credentials .csv file.  
**DATASET_NAME** | Enter the ID of the Personalization dataset that contains the segment you’re exporting, such as engage.  
**Port** | Enter 22.  
**Username** | Copy and paste the SFTP username from the .csv file you downloaded when you created the SFTP account.  
**Auth Type** | Select **Password** from the dropdown.  
**Password** | Copy and paste the SFTP password from the .csv file you downloaded when you created the SFTP account.  
**Retype Password** | Copy and paste the SFTP password from the .csv file you downloaded when you created the SFTP account.  
  
  6. Click **Save**.
  7. Repeat this process for each dataset that you have, such as Test Outbound and Production Outbound.

Previous

**[Export a Segment to Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_marketing_cloud_steps.htm&language=en_US&type=5
"Set up a nightly feed or a one-time export to synchronize Personalization
segments with Marketing Cloud. For example, you can synchronize a segment to
Marketing Cloud to target a specific group with an email communication.")**

Next

**[Create a Target Data Extension in Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_load_marketing_cloud_extension.htm&language=en_US&type=5
"Set up a target data extension in Marketing Cloud to map the fields in the
segment that you’re exporting. After you create the data extension, save the
external key to set up data extracts in Automation Studio.")**

