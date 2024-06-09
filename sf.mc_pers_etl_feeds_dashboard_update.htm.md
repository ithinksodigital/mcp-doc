

# ETL Job Status During Software Release Updates

Marketing Cloud Personalization manages ETL jobs during software release
updates.

When a software release update is initiated, Personalization manages running
and queued jobs in the following manner.

  * For running ETL jobs, Personalization requests suspension of each executing job (**Pause Requested**), suspending execution at a logical stopping point, then changes the status to **Paused**. When jobs are paused, no new ETL jobs that modify objects of the same type are started. At an appropriate time after the software update completes, Personalization requests to resume processing of each paused ETL job (**Resume Requested**), preserving the job execution sequence that was in effect before the software release update. When a job resumes, processing picks up where it left off, with a new job ID that’s similar to the previous one, and its status returns to **Running**.
  * For queued ETL jobs, Personalization requests the cancellation of each queued job (**Cancel Requested**) and changes their status to **Canceled**. At an appropriate time after the software update completes, Personalization picks up **Canceled** jobs, creates a ETL job for each one, and queues them for processing. To ensure that Personalization loads data in the correct order, it requeues jobs in the same order in which they were initially received. If you notice that your **Queued** ETL jobs were canceled, check to see whether, for each canceled job, the same feed file is associated with a different job that is in a **Queued** or **Completed** state. If so, then you can conclude that a software release update occurred.

#### See Also

  * [Navigate the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard_use.htm&language=en_US&type=5 "Open the Feeds Dashboard and explore ETL jobs that are queued, in progress, or complete.")

