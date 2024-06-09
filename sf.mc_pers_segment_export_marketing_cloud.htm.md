

# Export Segments to Marketing Cloud

Configure a process in Marketing Cloud Automation Studio to automatically load
CSV export files from the Personalization system to Marketing Cloud data
extensions. Complete these tasks in sequence.

  1. **[Export a Segment to Marketing Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_marketing_cloud_steps.htm&language=en_US&type=5)**  
Set up a nightly feed or a one-time export to synchronize Personalization
segments with Marketing Cloud. For example, you can synchronize a segment to
Marketing Cloud to target a specific group with an email communication.

  2. **[Connect the Personalization SFTP to Marketing Cloud for Segment Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_sftp_load_marketing_cloud.htm&language=en_US&type=5)**  
To receive Personalization segments, configure the Personalization SFTP in
Marketing Cloud. You can create a file location and add your existing SFTP
account details.

  3. **[Create a Target Data Extension in Marketing Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_load_marketing_cloud_extension.htm&language=en_US&type=5)**  
Set up a target data extension in Marketing Cloud to map the fields in the
segment that you’re exporting. After you create the data extension, save the
external key to set up data extracts in Automation Studio.

  4. **[Find a Segment’s ID](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_id_find.htm&language=en_US&type=5)**  
You use a segment’s ID when defining its automation process in Automation
Studio. There are also instances when you need a segment’s ID for an ETL data
feed.

  5. **[Define an Automation for Segment Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_automation_studio_load.htm&language=en_US&type=5)**  
Configure and schedule an automation for segment exports. You can also text
the automation before activating it.

