

# Import ETL Data Feeds from Marketing Cloud

Use Marketing Cloud Personalization ETL data feeds to import data from
Marketing Cloud Engagement. In Automation Studio, configure an automatic
process to export data from data extensions and load them directly into
Personalization. Before sending ETL data feeds from Marketing Cloud Engagement
to Personalization, make sure to first create an SFTP account.

  1. **[Connect the Personalization SFTP to Marketing Cloud for ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_connect_sftp.htm&language=en_US&type=5)**  
In Automation Studio, configure a process to automatically send CSV export
files from Marketing Cloud Engagement data extensions to Marketing Cloud
Personalization.

  2. **[Create a Source Data Extension in Marketing Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_source_data_extension.htm&language=en_US&type=5)**  
In Automation Studio, configure a process to automatically load CSV export
files from Marketing Cloud Engagement data extensions into Marketing Cloud
Personalization using ETL data feeds.

  3. **[Load Data to a Source Data Extension](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_source_data_extension_load.htm&language=en_US&type=5)**  
Use a SQL query to retrieve data from other data extensions and standard views
of Marketing Cloud Engagement, transform the data to the required format, and
save it to the source data extension.

  4. **[Define a Personalization ETL Data Feed Automation](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_load_automated.htm&language=en_US&type=5)**  
In Automation Studio, configure an automation process to load CSV export files
from Marketing Cloud Engagement data extensions to Personalization, and encode
them using UTF-8.

#### See Also

  * [Create an SFTP Account](https://help.salesforce.com/s/articleView?id=sf.mc_pers_sftp_account_create.htm&language=en_US&type=5 "Send and receive data from an automated platform safely and securely using ETL Integration. After you create an SFTP account, add the credentials to your FTP client.")

