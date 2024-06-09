

# Integrate Personalization with Account Engagement

Share data between Marketing Cloud Personalization and Marketing Cloud Account
Engagement. Send segments and Open Time email components to Account
Engagement. Receive ETL data feeds from Account Engagement for user, user
attributes, and campaign events data.

## Integration Overview

Integration Feature  | Description   
---|---  
Direction | To and from Marketing Cloud Account Engagement  
Integration Type (Inbound) | Inbound data from Marketing Cloud Account Engagement:

  * Feed

  
Integration Type (Outbound) | Outbound data to Marketing Cloud Account Engagement: 

  * File-based
  * Copy and paste Open Time Email HTML

  
Data Synchronization | Nightly or one-off file transferOpen-time email is real time  
  
## How Integration Works

Type of Data | Description  
---|---  
Segment push | Use Personalization’s Segment Exporter Gear to push segments to the Personalization SFTP so you can pull them into Marketing Cloud Account Engagement for enhanced targeting. For more information, see [Export a Segment to the Personalization SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5 "Set up a nightly feed or a one-time export to synchronize segments with the Personalization SFTP. You can then use these segments in other systems to target cross-channel communications. For example, you can synchronize a segment to Marketing Cloud to target a specific group with an email communication.").  
User and campaign data | Use Personalization’s ETL Integration to store users, user attributes, and campaign events, such as sends, opens, and clicks. For more information, see [About ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration_about.htm&language=en_US&type=5 "Learn more about loading data into Marketing Cloud Personalization.").  
Open-time email | Power Marketing Cloud Account Engagement email with 1:1 offers or content and product recommendations at open time. For more information, see [Create an Open Time Email Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_create.htm&language=en_US&type=5 "Generate a block of HTML code for an Open Time Email campaign and use it in your existing email marketing service to add personalized content for each recipient. After creating an Open Time Email campaign, you can clone it and reuse it with the same recipe for additional campaigns. You can also add exclusions and inclusions to your campaigns to tailor them to your overall email strategy.").  
  
#### See Also

  * [Open Time Email Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign.htm&language=en_US&type=5 "Use open time email campaigns to deliver personalized content and product recommendations each time a recipient opens an email. Using existing email campaigns that you send using your mail marketing service, Open Time Email campaigns deliver real-time personalized content to each member of your subscriber list.")
  * [Market to Your Customers with Account Engagement](https://help.salesforce.com/s/articleView?id=sf.bundle_pardot_parent.htm&language=en_US&type=5)

