

# About ETL Data Feeds

Learn more about loading data into Marketing Cloud Personalization.

## What Does ETL Stand For?

ETL stands for Extract, Transform, and Load. In Personalization, ETL
integration refers to the framework for bulk ingesting data (including
Salesforce data) into the platform from external sources. Begin by providing a
CSV file that contains the rows of data you want to ingest, formatted
according to our specifications. During ETL processing, Personalization
extracts the data from that file, transforms the data in each row, and then
loads the transformed data into the platform.

## What's a Feed?

A feed is a pathway to send structured, current, and up-to-date information
from one system to another. After a feed is configured, you can view and
manage it from the Marketing Cloud Personalization Feeds Dashboard.

## ETL Files

A Comma-Separated Values (CSV) file is a plain text file that contains rows of
data to ingest. The CSV file can be encrypted or compressed. The CSV file must
comply with our schema and formatting specifications. For more information,
see [ETL File
Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5
"ETL files contain entries such as users, products, subscription list members,
promotions, transactions, and more. These files must be in a CSV format and
can be encrypted or compressed. The file formats must follow the explicit
schema requirements for each ETL data feed. Typically, you upload ETL files
automatically using the SFTP site, but you can also manually upload a file.")
and [Available ETL Data
Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5
"Use these ETL data feeds for ETL integration.").

## Create an SFTP Account

SFTP is a file protocol for transferring large files securely over the web
using encryption and authentication. To use ETL data feeds with SFTP, you must
[Create an SFTP
Account](https://help.salesforce.com/s/articleView?id=sf.mc_pers_sftp_account_create.htm&language=en_US&type=5
"Send and receive data from an automated platform safely and securely using
ETL Integration. After you create an SFTP account, add the credentials to your
FTP client.").

## Steps to Ingest Data Using ETL Data Feeds

The ETL data feed process consists of the following high-level steps:

# | Description  
---|---  
1 | Start with a large amount of data from an external system that you want to get into Personalization, such as product updates for your catalog.  
2 | Extract data from your external system and create a CSV file using the required schema for the applicable ETL data feed, such as the [Product ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_product_data_feed.htm&language=en_US&type=5 "Use the Product ETL data feed to update the products in your catalog and to add new products.").  
3 | When the ETL file is ready, Salesforce developers create an automatic processing job to upload the file to the Inbound folder of your configured Personalization SFTP site.  
4 | Activate the ETL data feed so it automatically pulls files from the Inbound folder on the SFTP site based on their filenames. Files don’t process unless the filenames match the defined structure of the ETL data feed schemas.  
5 | Your processing job runs automatically and the ETL file moves from Inbound to Processing to Processed, which you can monitor on the Feeds Dashboard. You can’t manually move ETL files.  
6 | Jobs of different types that don’t affect shared data types can process concurrently. For example, one dataset can have a User ETL job and a Product ETL job processing simultaneously. However, neither of those jobs can run at the same time as a Transaction ETL job because the Transaction ETL data feed impacts both users and products.  
7 | Processing of ETL files doesn't impact ongoing updates from the Marketing Cloud Personalization module of the Salesforce Interactions SDK or Event APIs.  
8 | Personalization retains SFTP files for 60 days and then automatically purges them. This policy ensures compliance with regulations and reduces risk from persisted data. Personalization retains all files, even if they failed to process or contain incorrect data. You can delete files manually from your FTP client.  
  
## Automatic and Manual File Ingest

ETL feeds are automatically triggered by file uploads into the Inbound folder
of the SFTP site. After the file is uploaded into SFTP, MCP detects the
presence of the uploaded file, then begins the file-processing procedure. For
test files, ETL uploads can be run manually, as described in [Upload an ETL
File
Manually](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_upload.htm&language=en_US&type=5
"ETL data feeds are commonly configured to automatically upload the ETL files
using the SFTP site. However, you can upload files manually if, for example,
you want to ingest data that doesn’t get updated frequently, or if you want to
confirm the .CSV file format without committing changes.").

