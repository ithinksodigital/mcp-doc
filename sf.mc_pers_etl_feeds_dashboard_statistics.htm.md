

# ETL Processing Statistics

While processing an ETL job, Personalization continuously tabulates and
displays statistics for the job in progress.

Statistic | Description  
---|---  
**Extracted** | Number of rows that Personalization has extracted from feed files during the ETL job. For ETL feeds in which multiple rows are transformed for an object, this value can exceed the Transformed value.  
**Transformed** | Number of objects to which Personalization has applied the changes from the ETL feed.  
Loading Statistics: | -  
**Staged** | Number of objects staged. For test ETL runs, Personalization stages but doesn’t commit the changes. Otherwise, objects are staged and committed at the same time.  
**Commits** | The number of objects in the system that Personalization has committed. Commits apply to operations that overwrite existing Personalization data with new data from the feed file. With a live streaming feed, such as from the FTP service, commits occur automatically.  
**Success** | Number of successful commits to the rest of the system.  
  
#### See Also

  * [Navigate the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard_use.htm&language=en_US&type=5 "Open the Feeds Dashboard and explore ETL jobs that are queued, in progress, or complete.")

