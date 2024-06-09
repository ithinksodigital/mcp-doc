

# Data Cloud Activation ETL Data Feed

Use the Data Cloud Activation ETL data feed (SalesforceCDPActivationETL) to
import user profile and segment data from Data Cloud into Marketing Cloud
Personalization using Data Cloud’s Marketing Cloud Personalization Connector.

## About Data Cloud Activation

The CDP Activation ETL feed (SalesforceCDPActivationETL) is used exclusively
to support [Data Cloud's Marketing Cloud Personalization
Connector](https://help.salesforce.com/s/articleView?id=sf.c360_a_interaction_studio_connector.htm&language=en_US&type=5).

## Requirements

Set up activation in Data Cloud according to the instructions in [Set Up a
Connection to Marketing Cloud
Personalization](https://help.salesforce.com/s/articleView?id=sf.c360_a_set_up_interaction_studio_connector.htm&language=en_US&type=5).

In the Data Cloud activation, you must include at least one Marketing Cloud
Personalization identity attribute.

  * In Data Cloud activation, Email Address is the default setting on the activation. In Personalization, `emailAddress` is the default identity attribute name. For default attributes that are included in the activation, you don’t need to enter a preferred attribute name. The Data Cloud Email Address value automatically maps to the Personalization `emailAddress` identity attribute value.
  * To use additional attributes as identifiers in the activation, add the attribute and its preferred attribute name to the activation setup. The preferred attribute name must match an identity attribute name in Personalization exactly.
  * If a user in the activation isn’t added as expected to the segment in Personalization, it’s possible that
    * they don’t have any identity attributes in the file, and
    * their subscriber key value doesn’t match any existing profile ID value in Personalization.
This scenario can result in different counts of individuals between the Data
Cloud segment and the Personalization segment. Count differences can occur
because identity merges in Personalization that are based on identity
attributes included in the activation can also contribute to a difference in
the final segment member count.

  * Any attributes that you add to the activation must have a preferred attribute name that matches the name of an existing attribute in the target Personalization dataset. The activation doesn’t create attributes in Personalization. Attribute names in Personalization are case-sensitive. If the preferred attribute name in the activation doesn’t match an attribute in Personalization, then the job throws errors, and the activation can fail if the error threshold is exceeded.

## Data Cloud Activation Success Precedes Ingestion into Personalization

Activation success in Data Cloud means only that Data Cloud successfully
posted the activation file to the SFTP for ingestion by Personalization. It
doesn’t mean that Personalization successfully ingested the activation file.

## Monitoring an Activation Job in Personalization

  * To monitor a job in Personalization, navigate to the Feeds Dashboard page in the target Personalization dataset. On the left side of the Feeds Dashboard, under the Feeds column, select **SalesforceCDPActivationETL**.
  * To see the filename associated with a specific activation feed, click the feed in the SalesforceCDPActivationETL History tab. The filename starts with the Activation ID.
  * To view other information or to troubleshoot a feed, click **Review Execution** on the SalesforceCDPActivationETL History tab. On the page that opens, to view the feed's log, click the Log tab. Inside the log, show additional information by clicking the dropdown next to **com.apptegic.excavate.domain.jobs.gears.EtlProcessingDatasetJob**. Scroll to view the activation ID and batch ID.
  * If the feed job fails, view error messages in the **consoleLine** tab. The file name appears under the file name information.

#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")
  * [ETL Ingestion Performance](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_performance.htm&language=en_US&type=5 "Marketing Cloud Personalization doesn’t guarantee a throughput rate for ETL ingestion, so it’s helpful to know which factors can affect ETL ingestion rates. Many of these factors depend on the type of record that the feed modifies. ETL processing speeds vary across accounts and datasets.")
  * [Import Data from Data Cloud Into Personalization](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_cdp_import.htm&language=en_US&type=5 "Ingest Salesforce Data Cloud profile and segment data into Marketing Cloud Personalization.")
  * [ _Data Cloud Documentation:_ Create a Marketing Cloud Personalization Activation Target](https://help.salesforce.com/s/articleView?id=sf.c360_a_create_mc_personalization_activation_target.htm&language=en_US&type=5)

