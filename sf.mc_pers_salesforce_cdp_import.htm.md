

# Import Data from Data Cloud Into Personalization

Ingest Salesforce Data Cloud profile and segment data into Marketing Cloud
Personalization.

## How Integration Works

  * In Data Cloud, Data Cloud activation jobs collect segment membership, selected attributes, and calculated insights. Data Cloud transforms the data into .csv files and a JSON file, and then sends it to Personalization through a shared file store.
  * In Personalization, the Data Cloud Activation ETL data feed imports the data as user attributes and manual segments.
  * Data synchronization occurs at 12- or 24-hour intervals. The cadence is tied to the Data Cloud segment publish schedule. For more information, see [Publish a Segment in Data Cloud](https://help.salesforce.com/s/articleView?id=sf.c360_a_publish_segment.htm&language=en_US&type=5). 

## Target Personalization Web and Mobile Campaigns to Data Cloud Segments

To integrate Data Cloud segments with your Personalization campaigns, complete
the following tasks in Data Cloud:

Task in Data Cloud | Description  
---|---  
[Set Up a Connection to Marketing Cloud Personalization](https://help.salesforce.com/s/articleView?id=sf.c360_a_set_up_interaction_studio_connector.htm&language=en_US&type=5) | Connect to your Personalization account for use in Data Cloud.   
[Create and activate a segment](https://help.salesforce.com/s/articleView?id=sf.c360_a_segments.htm&language=en_US&type=5) | Create a segment of users for activation targeting.  
[Create an activation](https://help.salesforce.com/s/articleView?id=sf.c360_a_activation.htm&language=en_US&type=5) | When you create an activation, you choose the segment, activation membership, and activation target, and then select channel contact points for the activation. You can add and manage attributes in the activation, such as email address. In the Data Cloud activation, you must include at least one Marketing Cloud Personalization identity attribute. For more information, see Requirements in [Data Cloud Activation ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_activation_data_feed.htm&language=en_US&type=5 "Use the Data Cloud Activation ETL data feed \(SalesforceCDPActivationETL\) to import user profile and segment data from Data Cloud into Marketing Cloud Personalization using Data Cloud’s Marketing Cloud Personalization Connector.").  
  
## Use Case Example: Use Data Cloud’s Calculated Insights

Use Calculated Insights to build expressions for personalization campaigns.
Expressions provide additional flexibility with expanded profile or engagement
data beyond Personalization’s data model or engagement scoring. For more
information, see [Calculated
Insights](https://help.salesforce.com/s/articleView?id=sf.c360_a_calculated_insights.htm&language=en_US&type=5).

Type of Information | Examples  
---|---  
Banded tiers | High, medium, and low lifetime value (LTV)  
Sliding window calculations | Days until renewal, points until next reward, number of open opportunities and cases  
Custom engagement scores | Such as business-defined affinity  
  
## Use Case Example: Use Data Cloud’s Unified Individual

Use Data Cloud’s Unified Individual to create automated feeds of cross-cloud
identities and attributes. Automated feeds allow you to share details from
Sales, Service, and Marketing Cloud Engagement to drive decisions in
Personalization. For more information, see [Unified Individual for Activate
Membership](https://help.salesforce.com/s/articleView?id=sf.c360_a_unified_profile_activation.htm&language=en_US&type=5).

Type of Data | Examples  
---|---  
Marketing Cloud Engagement contacts | Contact Keys and Einstein Engagement Scores  
CRM leads and contacts | CRM ID along with name, contact information, next opportunity target close date  
Loyalty Cloud | Loyalty contacts with points and status

