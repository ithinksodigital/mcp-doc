

# Feed Processing Status for Running ETL Jobs

The Feeds Dashboard displays the status of running ETL jobs.

Status | Description  
---|---  
**Initialized** | The ETL feed job has been requested. After a job is initialized, it proceeds to either: 

  * **Preparing** if it’s starting to run, or
  * **Queued** if another job is running.

  
**Queued** | The ETL job is queued and ready to process at the next available opportunity. Personalization queues an ETL job if another ETL job, currently in progress, is updating the same type of objects that the **Queued** ETL job will update.  
**Preparing** | Personalization makes sure the ETL job can run properly before starting to process the data. This status appears after **Initialized** or **Queued** and before **Running**.  
**Running** | The ETL job is processing and loading data into the Personalization system. The feed file temporarily resides in the “processing” folder.  
  
#### See Also

  * [Navigate the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard_use.htm&language=en_US&type=5 "Open the Feeds Dashboard and explore ETL jobs that are queued, in progress, or complete.")

