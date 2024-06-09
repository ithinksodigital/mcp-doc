

# About Integrating with Third-Party Solutions

Marketing Cloud Personalization integrates with a variety of third-party
solutions (external to Salesforce). Integration options include data
management platforms, email service providers, third-party campaign detection
products, analytics products, content management systems, social media, and
tag managers.

## Data Management Platforms (DMP)

Application Examples  | Integration Type  | Data Synchronization  | How It Works   
---|---|---|---  
  
  * Adobe Audience Manager
  * BlueKai
  * Neustar

|  Data into Personalization:

  * Client-side sync
  * ETL data feeds

Data out to a DMP platform:

  * File-based
  * Campaign exposure

| Data in:Files posted to the Personalization SFTP site are processed on an ongoing basis.Data out:Segment export is nightly or one-off. | 

  * Personalization doesn’t currently have any server-to-server integrations with DMP platforms. DMP integrations are client-side only.
  * Attributes and segment IDs can be passed to Personalization and stored as custom user profile attributes.
  * Personalization can also pass segment membership data to the page for a DMP to collect and use for retargeting efforts.

For more information, see [Export a Segment to the Personalization
SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5
"Set up a nightly feed or a one-time export to synchronize segments with the
Personalization SFTP. You can then use these segments in other systems to
target cross-channel communications. For example, you can synchronize a
segment to Marketing Cloud to target a specific group with an email
communication.") and [About ETL Data
Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration_about.htm&language=en_US&type=5
"Learn more about loading data into Marketing Cloud Personalization.").  
  
## Email Service Providers (ESP)

Application Examples  | Integration Type  |  Data Synchronization  | How It Works  
---|---|---|---  
  
  * Yes Lifecycle Marketing
  * Silverpop
  * Cheetah Mail
  * Adobe Campaign

| Data in to Personalization:

  * ETL data feeds

Data out to an ESP platform:

  * File-based
  * Open-time email

| Data in:

  * Files posted to the Personalization SFTP site are processed on an ongoing basis.

Data out:

  * Segment export is nightly or one-off.

|

  * Segments—Use Personalization’s Segment Exporter Gear to push segments to the Personalization SFTP so you can pull them into your ESP for enhanced targeting. For more information, see [Export a Segment to the Personalization SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5 "Set up a nightly feed or a one-time export to synchronize segments with the Personalization SFTP. You can then use these segments in other systems to target cross-channel communications. For example, you can synchronize a segment to Marketing Cloud to target a specific group with an email communication.").
  * User and Campaign Data—Use Personalization’s [Account ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_account_data_feed.htm&language=en_US&type=5 "Use the Account ETL data feed to update account information in Unified Account Profiles.") to store users, user attributes, and campaign events, such as sends, opens, and clicks.
  * Open-time email—Create an email campaign to power 1:1 offers or content and product recommendations at open time within your ESP. For more information, see [Create an Open Time Email Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_create.htm&language=en_US&type=5 "Generate a block of HTML code for an Open Time Email campaign and use it in your existing email marketing service to add personalized content for each recipient. After creating an Open Time Email campaign, you can clone it and reuse it with the same recipe for additional campaigns. You can also add exclusions and inclusions to your campaigns to tailor them to your overall email strategy."). 

  
  
## Third-Party Campaign Detection

Application Examples  | Integration Type  | Data Synchronization  | How It Works   
---|---|---|---  
UTM parameter mapping | UTM parameter mapping | Real time upon click-through | 

  * Use an existing product or add one to configure the UTM parameter mapping.
  * To capture any additional information you’re sending through your campaigns, add parameters. Mapping tells Personalization how to align query parameters in the landing page URL to attributes on the Personalization external campaign, or to attributes defined for the referred visitor. For more information, see [UTM Parameter Mapping](https://help.salesforce.com/s/articleView?id=sf.mc_pers_third_party_utm_parameter_mapping.htm&language=en_US&type=5 "UTM parameters are customizable codes that you use in URLs and links to track and measure the success of various aspects of your third-party campaigns. UTM parameters can track traffic, referral sources, external campaigns, keywords, and content zones.").
  * As users arrive on the landing page that contains the third-party product integration, external campaigns appear on the Third-Party campaign list page in the Uncategorized folder.
  * The external campaigns have click-throughs, but not impressions because Personalization doesn’t track impressions for external campaigns.
  * Campaign engagement is available to reference in segmentation to further enhance experience targeting.

  
  
## Analytics

Application Examples  | Integration Type  | Data Synchronization  | How It Works   
---|---|---|---  
  
  * Adobe Analytics
  * Google Analytics

| Client-side sync | Real-time in-browser | Personalization can listen for campaign statistics events that you can use to format events for third-party tracking systems. For more information, see [Sending Campaign Stats to Third Parties](https://developer.salesforce.com/docs/marketing/personalization/guide/campaign-stats-tracking.html?q=data+campaign+stat+events#sending-campaign-stats-to-third-parties).  
  
## Content Management Systems (CMS)

Application Examples  | How It Works   
---|---  
Typically, Personalization doesn’t require an integration with a CMS. | 

  * The [Web Site Personalization](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_sdk_integration.htm&language=en_US&type=5 "Integrate Marketing Cloud Personalization with your organization's web site. During implementation, your development team works with Salesforce to create your organization’s site map and plan your web integration.") creates a reference catalog of product and content assets by scraping the page directly.
  * Personalization can ingest additional content and product information, and promotion assets, using [ETL Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_integration.htm&language=en_US&type=5 "Ingest data into Marketing Cloud Personalization using ETL data feeds. ETL integration lets you batch load data using CSV files that are generated externally. Update the catalog, import and export segments, upload historical data, and more. You import CSV files using an SFTP site or uploading them manually.").
  * Personalization can render both client-side and server-side campaigns and experiences.
  * The Salesforce Interactions SDK Launcher doesn’t support integration with CMS solutions (such as Oracle CMS) that use the `document.write()` method in the DOM Web API to modify the active page. The [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/API/Document/write) also discourages the use of this method.

  
  
## Social

Application Examples  | Integration Type  | Data Synchronization  | How It Works  
---|---|---|---  
Generic segment sync  | File-based  | One-off or nightly  | Pass segments out of Personalization by SFTP into various media and display tools for enhanced retargeting efforts. For more information, see [Export a Segment to the Personalization SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5 "Set up a nightly feed or a one-time export to synchronize segments with the Personalization SFTP. You can then use these segments in other systems to target cross-channel communications. For example, you can synchronize a segment to Marketing Cloud to target a specific group with an email communication.").   
  
## Tag Managers

You can implement Personalization to use a tag manager. As part of your
implementation process, work with your implementation team to determine the
implementation approach that works best for you.

