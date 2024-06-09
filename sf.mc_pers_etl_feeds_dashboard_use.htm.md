

# Navigate the Feeds Dashboard

Open the Feeds Dashboard and explore ETL jobs that are queued, in progress, or
complete.

### Required User Permissions

Permissions Needed  
---  
To upload an ETL file: | A role with Administrator permissions  
  
  1. From the Gears section in the main navigation, select **Feeds** | **Feeds Dashboard**. The Feeds Dashboard opens in a new tab.

The **Feeds** sidebar lists all the configured ETL data feeds for your
organization.

The **History** area shows how many files were uploaded and how many records
were updated during the past 30 days for a selected ETL data feed.

The table displays a summary of the individual ETL jobs that Personalization
processed, is processing (in-progress jobs), or is queued for processing.
Table rows default to reverse chronological order, with the most recent at the
top. The table includes the following columns:

Column | Description  
---|---  
**Start Time** | Date/time when the ETL feed job was started or queued.  
**Run Time** | Duration of the ETL feed job.  
**Status** | Status of the ETL feed job. See [Feed Processing Status for Running ETL Jobs](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard_status.htm&language=en_US&type=5 "The Feeds Dashboard displays the status of running ETL jobs.") and [Processing Outcome Status for ETL Jobs That Have Reached Terminal Status](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard_outcome.htm&language=en_US&type=5 "When an ETL job finishes \(successfully or not\), it reaches a Terminal status. After an ETL job has reached a Terminal status, Personalization won’t change its status again.").  
**Job Progress** | Current progress (percent complete) of the ETL feed job. A completed job is 100%. If the job stopped running (for example, an error), this shows the percentage complete when the job was interrupted.  
**Total Rows** | Number of rows processed from the ETL feed file.  
**Extract Success** | Number of rows successfully extracted from the ETL feed file.  
**Transform Success** | Number of rows successfully transformed from the ETL feed file.  
**Commit Count** | Number of objects successfully committed from the ETL feed file.  
  
  2. To sort the table, click the column headers.
  3. To see additional information about a job, select it in the table.

The details section shows the filename, batch ID, successes, and errors.

  4. To see the individual columns and rows of the ETL file for the selected ETL job, click **Review Execution**. From this window, click **Logs** to view the processing logs for the ETL job and review any errors.
  5. To view the logs in real time while a job is in progress, click **Review Execution**.

A status of **TBD** in the Start Time column indicates that a job hasn’t
started processing. This status also appears if you run a test of an ETL file
that results in an error and file extraction doesn’t complete.

As long as ETL jobs aren’t updating the same objects, they can run in
parallel. For example, User ETLs can run at the same time as Product ETLs
because they update different objects. However, User ETLs can't run at the
same time as Transaction ETLs because they both modify User Profiles.

Alternatively, you can upload an ETL file manually from the Feeds Dashboard.
Manual uploads are helpful when you want to confirm the format of an ETL file,
and when you don't have a frequent amount of data to upload. For more
information, see [Upload an ETL File
Manually](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_upload.htm&language=en_US&type=5
"ETL data feeds are commonly configured to automatically upload the ETL files
using the SFTP site. However, you can upload files manually if, for example,
you want to ingest data that doesn’t get updated frequently, or if you want to
confirm the .CSV file format without committing changes.").

