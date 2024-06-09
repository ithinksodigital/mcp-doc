

# Processing Outcome Status for ETL Jobs That Have Reached Terminal Status

When an ETL job finishes (successfully or not), it reaches a **Terminal**
status. After an ETL job has reached a **Terminal** status, Personalization
won’t change its status again.

The following table describes status indicators for ETL jobs that have reached
**Terminal** status.

Status | Description  
---|---  
**Complete** | Personalization has successfully completed loading and processing data from the feed file. Personalization moves the feed file to the "processed" folder.  
**Error** | An error occurred during processing. A job fails entirely if the error threshold reaches 10%. An error can result from one of the following factors: 

  * Malformed feed file. The data doesn’t conform to our ETL file requirements as described in [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file."). For a specific ETL feed type, see [Available ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5 "Use these ETL data feeds for ETL integration.") to check that the header labels are spelled correctly and that the data is in the proper format.
  * System error. An issue occurred in the Personalization system. Try uploading the file again.

When a running ETL job results in an error, Personalization moves the feed
file to the “failed” folder. If another job is **Queued** , Personalization
automatically starts that **Queued** job. When a queued job results in an
error, the file remains. A new job tries to queue it for processing.  
**Canceled** | The ETL job was canceled during processing. An ETL job can be canceled in one of the following ways: 

  * User canceled. A user requested that Personalization cancel the ETL job.
  * System canceled. Canceling can occur when a **Queued** ETL job is canceled during a software release (**Release** status). 

  
**Resumed** | Personalization has created a separate ETL job to resume processing the feed file associated with this ETL job. The new ETL job contains all future updates for this ETL file. This ETL job remains in the Feeds Dashboard Past Runs for historical and logging purposes.  
  
#### See Also

  * [Navigate the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard_use.htm&language=en_US&type=5 "Open the Feeds Dashboard and explore ETL jobs that are queued, in progress, or complete.")

