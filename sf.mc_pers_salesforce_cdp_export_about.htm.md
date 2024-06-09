

# About Exporting Personalization Data to Data Cloud

Learn about exporting Personalization user and event data to Salesforce Data
Cloud.

## How Integration Works

  * Personalization collects user and event data. Personalization transforms the data into a .csv file and sends it to Data Cloud through a shared file store. Personalization streams event data to Data Cloud in near real-time.
  * Data Cloud imports the data using a Marketing Cloud Personalization data stream. Data Cloud ingests the data according to its data stream schedule. For details, see [Data Stream Schedule in Data Cloud](https://help.salesforce.com/s/articleView?id=sf.c360_a_data_stream_schedule.htm&language=en_US&type=5).

## Use Personalization Event Data in Data Cloud

The process for integrating event data from Personalization with your Data
Cloud customer profiles includes the following tasks:

Task | Description  
---|---  
[Configure Anonymous Data Export](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_cdp_anonymous_data_export.htm&language=en_US&type=5) | Decide whether you want to include anonymous user and event data in the data stream. By default, Personalization exports only known user data.  
[Set Up a Connection to Marketing Cloud Personalization](https://help.salesforce.com/s/articleView?id=sf.c360_a_set_up_interaction_studio_connector.htm&language=en_US&type=5) | An administrator with the appropriate permissions creates the connection between the two systems in Data Cloud.  
[Create a Marketing Cloud Personalization Data Stream](https://help.salesforce.com/s/articleView?id=sf.c360_a_create_interaction_studio_starter_bundle.htm&language=en_US&type=5) | Use a Personalization starter bundle to begin the flow of data from Personalization to Data Cloud.  
Complete bundle mappings according to the instructions in [Marketing Cloud Personalization Bundle Mappings](https://help.salesforce.com/s/articleView?id=sf.c360_a_interaction_studio_bundle_mappings.htm&language=en_US&type=5) | Complete bundle mappings for data types not included in the standard data stream. When you create a data stream using a Personalization starter bundle, the system creates standard mappings for you. However, there are a few data types that aren’t included and must be mapped. Any data type edits you make in Personalization after data stream creation and deployment aren’t reflected in your stream.

