

# Upload an ETL File Manually

ETL data feeds are commonly configured to automatically upload the ETL files
using the SFTP site. However, you can upload files manually if, for example,
you want to ingest data that doesn’t get updated frequently, or if you want to
confirm the .CSV file format without committing changes.

### Required User Permissions

Permissions Needed  
---  
To upload an ETL file: | A role with Administrator permissions  
  
  1. From the main navigation, select **Feeds** | **Feeds Dashboard**. The Feeds Dashboard opens in a new tab.
  2. Select the desired ETL data feed from the list of available feeds.
  3. Click **Validate** | **or** | **Execute**.
  4. To select a file that you previously manually uploaded, click **Select File** and navigate to the **Testing** folder to select the file.
  5. To select a new file to upload, click **Upload File** and navigate to the desired file to upload it. After the file successfully uploads, Personalization shows a confirmation message and the data appears in the File Data section. 

![5645bc92-6407-45bf-9369-148c9877deb8]

Note When uploading a new ETL file, make sure the file is in .csv format and
that it meets the schema requirements for the selected ETL data feed.

  6. In the **Review Staged Changes** section, click **Run Test** (not available for User ETL). Details about the file’s successes and errors appear.

Item | Description  
---|---  
**Extracted** | Indicates the number of rows that were successfully extracted from your file, and the number of rows that have errors.  
**Staged** | Indicates the number of rows that the file adds when you commit changes.  
  
  7. Review any file additions, changes, and deletions below the **Run Test** button (not available for User ETL).

Row Appearance | Meaning  
---|---  
blue row | Indicates modified data to update.  
green row | Indicates new data to add.  
red row | Indicates data to remove.  
Rows without highlights | Have no effect on the existing data.  
  
  8. To download a CSV file that indicates the data that the file affects, click the **Export** button.
  9. To add the data to Personalization, click **Commit**.

![3a8d25f8-0bfd-429a-a6f4-507310e326ab]

Note If you’re just testing an ETL file, don’t commit the data.

