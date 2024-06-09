

# FAQs for ETL Integration

Answers to frequently asked questions about ETL integration in Marketing Cloud
Personalization.

## File Processing

Question | Answer  
---|---  
How can I tell if my ETL job is running? | On the Feeds Dashboard, select an ETL type to see a historical list of jobs associated with that type, sorted descending by date, including any in-progress jobs. You see in-progress jobs at the top of the list. If there are no in-progress or completed rows in the table, the ETL hasn’t processed any files. The Job Progress percentage indicates how far along the job has progressed, with anything above 0% and below 100% still in progress. You can review percent success rates of the Extract and Transform stages, as well as the commit counts. While a job is in-progress, you can review execution to view the logs in real time. For more information, see [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.").  
How do I know when the job is finished? | A job is finished when Job Progress has reached 100% on the Feeds Dashboard.  
Can I run concurrent ETL jobs? | Yes, as long as the jobs don't update a shared data type, and the jobs are within the top ten jobs in the inbound file folder. 

  * Feeds can't run concurrently if they update a shared data type. For example, if users are referenced in a feed file, another feed file that references users can't run at the same time.
  * Ten jobs are considered at a time from the inbound folder. Files in the inbound folder are sorted by filename.

Example: One dataset can have a User ETL job and a Product ETL job running
simultaneously. However, neither can run at the same time as a Transaction ETL
job because the Transaction ETL impacts both users and products.  
Does an ETL job block updates to its corresponding data type from the Marketing Cloud Personalization module of the Salesforce Interactions SDK or Event API? | No. Data coming from the Marketing Cloud Personalization module of the Salesforce Interactions SDK or Event API still update corresponding data types while an ETL is running.  
What does **TBD** mean in the Feeds Dashboard? | If there are multiple queued ETLs, you might see **TBD** in the Start Time column if the processing of the target file hasn’t started. Alternatively, if you run a test of an ETL that results in an error so file extraction doesn’t complete, you see **TBD** displayed in the Feeds Dashboard for that ETL job. This result can occur when, for example, there’s no target file selected, or if the target file is empty.  
  
## File Processing Errors

Question | Answer  
---|---  
Why aren't my files processing? | Files are automatically processed only when the file names are structured correctly and placed in the correct directory. For specifications by feed type, see [Available ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5 "Use these ETL data feeds for ETL integration.").  
How can I use the Feeds Dashboard to view errors during the transform stage? | To review the job logs that include specific error reports, click the **Review Execution** button while a specific batch is highlighted. For more information, see [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.").  
Is there an error threshold that can cause a job to fail entirely? | Yes. The job fails entirely if the error threshold reaches 10%.  
I have an error message that states "Extract failed most likely due to a column or line delimiter." What does this mean? | To be processed, the file must be a validly parsable CSV. If it contains character mistakes—such as double quotes not closed, or extra commas throughout a value—it’s possible that the file doesn’t parse correctly. The log includes the file line number that caused the error.  
I have an error message that states `Warning: At least one Product is archived. Updates won’t be visible in the UI.` What does this mean? | This error message can appear while you perform a product, category, or dimension/catalog object ETL upload. It means that at least one of the items in your ETL is in an archived state. An item becomes archived by doing one of the following: 

  * Click **Delete** next to the item in the Marketing Cloud Personalization catalog
  * Send an ETL with a column header of `attribute:archived` and a value of true

Archived items can’t be returned in any campaign and aren’t visible in the
Marketing Cloud Personalization catalog. If you want, you can have all items
in your ETL appear in the catalog and be available to return in a campaign
response. To unarchive any items that are currently in an archived state,
confirm that the `attribute:archived` column is in your ETL file and has a
value of false.  
I have an error message that states `PolyglotException: At least one groupBy field is required.` What does this mean? | This error message can appear while processing an ETL feed in which the CSV is missing data in GroupBy fields. In ETL Feeds, Personalization uses GroupByFields to group objects together to make updates to the databases and system at the same time for that object. Each ETL file format has its own set of GroupByFields.For example, supposed you encounter this message while processing a User Profile Object feed file. This CSV feed groups groups by UserId and any IdentityFields. In this context, the message means that a userId or identity attribute header is not present. For more information, see [User Profile Object ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_profile_object_data_feed.htm&language=en_US&type=5 "Use the User Profile Object ETL data feed to update the user profile objects you create.").  
  
## File Requirements

Question | Answer  
---|---  
What are the character limit counts? | Character limit counts are defined in the specification documents for each available feed type. For more information, see [Available ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5 "Use these ETL data feeds for ETL integration.").  
What is the file size limit? | There’s no file size limit. However, Salesforce recommends limiting file sizes to 5 GB. For more information, see [Personalization Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_limits.htm&language=en_US&type=5 "Learn about the limits and capabilities in Marketing Cloud Personalization.").  
  
## Data Management

Question | Answer  
---|---  
Can I unset a user attribute? | User ETLs are unique. Often, Personalization receives user data from multiple sources that are all canonical. Unlike Item Type ETLs, a blank value in the User ETL results in no change to the existing attribute value. For more information, see [User ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5 "Use the User ETL data feed to update Unified Custom Profiles, and Unified Account Profiles if you have B2B Detect. Personalization stores user profiles for each anonymous and known user in the system.").  
My ETL job appears to have run, but items aren’t listed in the catalog. I see only 100 items on the item list page, but my file contained many thousands of items. Is everything working correctly? | When a catalog has more than 10,000 of an item, only items with item actions, such as a view or a purchase, show up on the catalog list screen. You can still visit catalog edit pages directly by editing the item ID query string of an item edit page. Items that have no views or actions attached are hidden from the catalog.   
Can I clear all commits related to a recent ETL job? | Due to data retention policies, Personalization can’t clear commits related to a recent load. You can unset values and attributes as allowed by the ETL type, but Personalization can't "clean up" incorrect or incorrectly loaded data.  
The ETL file completed successfully, but I don't see the updates applied to changed products. Is there anything I can check? | Product updates through ETL or the Marketing Cloud Personalization module of the Salesforce Interactions SDK or Event API don’t get applied if the product is locked, which occurs when someone manually edits the product's information and saves changes. The assumption is that a manual edit is intentional and should take precedence over any inbound data source. When you edit a product page, the page appears to be locked in the top right-hand corner, but it remains locked only if you save an edit. To see if a product is locked, navigate to the product catalog (**Catalog > Products**). Find the item on the overview screen, and look for the lock icon that appears next to the product name in the right-hand column (right under the **Delete** button). If the product is locked, double-click to edit the product, select **Unlocked** from the dropdown in the top right, and click **Save**. Unlocking the product allows manual changes (and other unchanged attributes) to be updated by ETL, the Marketing Cloud Personalization module of the Salesforce Interactions SDK, or the Event API.  
  
## ETL Customization

Question | Answer  
---|---  
Can ETLs be customized? | No. ETLs can’t be customized by Personalization support, partners, or customers.  
How do I know what ETLs are available? | Available ETLs are all documented and available for review in [Available ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5 "Use these ETL data feeds for ETL integration.").  
Can I configure the error threshold for a specific ETL? | The error threshold is a constant value that can’t be configured.  
  
## SFTP Management

Question | Answer  
---|---  
Can I move a file from testing to inbound in the Feeds Dashboard? | Files can be placed in the inbound directory only by accessing the SFTP.

