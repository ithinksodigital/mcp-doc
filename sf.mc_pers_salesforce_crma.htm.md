

# Integrate Personalization with CRM Analytics

In Salesforce CRM Analytics, connect to Marketing Cloud Personalization’s Data
Warehouse and explore personalization data. Import prediction scores from CRM
Analytics into Personalization using ETL data feeds.

## About the Personalization Data Warehouse

![158e782e-0751-464c-bbb6-f02d189ebb92]

Note [](https://help.salesforce.com/s?language=en_US)The Data Warehouse is
available only for customers who have already purchased the Marketing Cloud
Personalization \- Data Warehouse add-on product.

The Personalization Data Warehouse contains personalization data that is
optimized for analysis and available in a preformatted schema. Marketing Cloud
Personalization provides daily updates to the Data Warehouse from its
operational data store.

## Integration Prerequisites

To gain access to the Personalization Data Warehouse, you need a user account
and connection information. You must also be added to the IP Allowlist. For
instructions, see [Set Up Access to the Personalization Data
Warehouse](https://help.salesforce.com/s/articleView?id=sf.mc_pers_data_warehouse_setup.htm&language=en_US&type=5
"Set up access to the Marketing Cloud Personalization Data Warehouse by
completing the following steps.").

## Connect and Explore Data

CRM Analytics connects to the Personalization Data Warehouse using its Amazon
Redshift connector (see [Amazon Redshift
Connection](https://help.salesforce.com/s/articleView?id=sf.bi_integrate_connectors_redshift_settings.htm&language=en_US&type=5)).

![3d636050-0faf-4ee0-a761-a16e00ce72a5]

After you’re connected, use SQL commands to explore the data in the Data
Warehouse. For schema details, see [Developer Documentation: Marketing Cloud
Personalization Data
Analytics](https://developer.salesforce.com/docs/marketing/personalization/guide/data-
analytics.html).

## Import Prediction Scores from CRM Analytics

Import predictive stores from CRM Analytics for use in segmentation and
targeting, or as input to feature engineering for Einstein Decisions.

Sequence | Task | Description  
---|---|---  
1 | Generate the Prediction Scores | Generate the prediction scores using Einstein Discovery. For instructions, see [Predict and Improve Outcomes](https://help.salesforce.com/s/articleView?id=sf.bi_edd_prediction.htm&language=en_US&type=5).  
2 | Create the File to Import | To prepare the file to import, use the data integration features in CRMA Analytics. For instructions, see [Integrate and Prepare Data for Analysis](https://help.salesforce.com/s/articleView?id=sf.bi_integrate_data_integration.htm&language=en_US&type=5). The file must comply with the specifications in [User ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5 "Use the User ETL data feed to update Unified Custom Profiles, and Unified Account Profiles if you have B2B Detect. Personalization stores user profiles for each anonymous and known user in the system.").  
3 | Upload the File Into Marketing Cloud Personalization | Upload the file, either as a one-off upload or posted to Personalization’s SFTP site for processing on a recurring (nightly) basis. For instructions, see [ETL Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration.htm&language=en_US&type=5 "Ingest data into Marketing Cloud Personalization using ETL data feeds. ETL integration lets you batch load data using CSV files that are generated externally. Update the catalog, import and export segments, upload historical data, and more. You import CSV files using an SFTP site or uploading them manually.").  
  
#### See Also

  * [Personalization Data Warehouse](https://help.salesforce.com/s/articleView?id=sf.mc_pers_data_warehouse.htm&language=en_US&type=5 "Marketing Cloud Personalization tracks and measures engagement—at the individual and account levels—across your company’s channels. The Data Warehouse is a repository of personalization data that is optimized for analysis. Business analysts can use their preferred business intelligence \(BI\) tool to access the Data Warehouse and run queries to transform, report on, analyze, and visualize your Marketing Cloud Personalization data.")
  * [ _Developer Documentation_ : Data Analytics](https://developer.salesforce.com/docs/marketing/personalization/guide/data-analytics.htm)

