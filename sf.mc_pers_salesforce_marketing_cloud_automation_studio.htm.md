

# Integrate Personalization with Automation Studio

Share data between Marketing Cloud Personalization and Marketing Cloud
Automation Studio. Import data from Automation Studio using ETL data feeds.
Export Personalization segments to Automation Studio.

## Integration Overview

Integration Feature  | Description  
---|---  
Direction | To and from Automation Studio  
Integration Type | File-based   
Data Synchronization | One-off or nightly  
  
## Import from Marketing Cloud Engagement

  * Use Personalization’s SFTP site as the file location.
  * Marketing Cloud Engagement data extensions are extracted using Personalization’s SFTP site as the destination in Automation Studio.
  * Personalization polls SFTP for new ETL files every 15 minutes for import.

For more information, see [About ETL Data
Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration_about.htm&language=en_US&type=5
"Learn more about loading data into Marketing Cloud Personalization.").

## Export to Marketing Cloud Engagement

  * Export from any Personalization segment.
  * The process uses the Segment Exporter Gear.
  * Exports to Personalization’s SFTP site.
  * Export types: manual (full or delta), nightly (delta)

For more information, see [Export Segments to Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_marketing_cloud.htm&language=en_US&type=5
"Configure a process in Marketing Cloud Automation Studio to automatically
load CSV export files from the Personalization system to Marketing Cloud data
extensions. Complete these tasks in sequence.").

#### See Also

  * [Marketing Cloud Automation Studio](https://help.salesforce.com/s/articleView?id=sf.mc_as_automation_studio.htm&language=en_US&type=5)

