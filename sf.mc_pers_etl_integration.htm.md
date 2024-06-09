

# ETL Integration

Ingest data into Marketing Cloud Personalization using ETL data feeds. ETL
integration lets you batch load data using CSV files that are generated
externally. Update the catalog, import and export segments, upload historical
data, and more. You import CSV files using an SFTP site or uploading them
manually.

  * **[About ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration_about.htm&language=en_US&type=5)**  
Learn more about loading data into Marketing Cloud Personalization.

  * **[Encrypt Sensitive Data](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration_encrypt.htm&language=en_US&type=5)**  
Use the Personalization public PGP key to encrypt sensitive data in your ETL
data feeds. Because Personalization uses a secure file transfer protocol
(SFTP) to process ETL data feeds, you don’t need to use PGP encryption unless
your organization requires it.

  * **[ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5)**  
ETL files contain entries such as users, products, subscription list members,
promotions, transactions, and more. These files must be in a CSV format and
can be encrypted or compressed. The file formats must follow the explicit
schema requirements for each ETL data feed. Typically, you upload ETL files
automatically using the SFTP site, but you can also manually upload a file.

  * **[Available ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5)**  
Use these ETL data feeds for ETL integration.

  * **[Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5)**  
The Feeds Dashboard provides details about ETL feed jobs.

  * **[Upload an ETL File Manually](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_upload.htm&language=en_US&type=5)**  
ETL data feeds are commonly configured to automatically upload the ETL files
using the SFTP site. However, you can upload files manually if, for example,
you want to ingest data that doesn’t get updated frequently, or if you want to
confirm the .CSV file format without committing changes.

  * **[Import ETL Data Feeds from Marketing Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_marketing_cloud_send_data_from.htm&language=en_US&type=5)**  
Use Marketing Cloud Personalization ETL data feeds to import data from
Marketing Cloud Engagement. In Automation Studio, configure an automatic
process to export data from data extensions and load them directly into
Personalization. Before sending ETL data feeds from Marketing Cloud Engagement
to Personalization, make sure to first create an SFTP account.

  * **[ETL Ingestion Performance](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_performance.htm&language=en_US&type=5)**  
Marketing Cloud Personalization doesn’t guarantee a throughput rate for ETL
ingestion, so it’s helpful to know which factors can affect ETL ingestion
rates. Many of these factors depend on the type of record that the feed
modifies. ETL processing speeds vary across accounts and datasets.

  * **[FAQs for ETL Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration_faq.htm&language=en_US&type=5)**  
Answers to frequently asked questions about ETL integration in Marketing Cloud
Personalization.

