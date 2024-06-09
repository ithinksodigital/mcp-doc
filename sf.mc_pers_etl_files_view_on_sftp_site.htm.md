

# View ETL Files on the SFTP Site

Review processed ETL files after creating SFTP accounts and beginning data
transfer. Personalization deletes files after 60 days.

### Required User Permissions

Permissions Needed  
---  
To view ETL files on the SFTP site: | A role with Administrator permissions  
  
You must have these IP addresses open:

  * 3.220.105.107 port 22
  * 54.87.171.233 port 22
  * 54.161.29.212 port 22

  1. From the main navigation, select **Feeds** | **SFTP Files.**
  2. Click the folder that you want to view. Files are in alphabetical, not chronological, order.

Folder | Description  
---|---  
Failed | The file failed to load due to a system error, such as missing headers or an incorrect file type.  
Inbound | The first destination for FTP files.  
Outbound | SFTP files exported from Personalization. Premium edition only.  
Processed | The file completed the import process.  
Processing | The file is in the middle of importing, which can take a variable amount of time based on the size of the file.  
Testing | The file is ready for review and testing before you commit any changes.  
  

