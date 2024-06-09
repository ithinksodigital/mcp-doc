

# Configure Personalization Gears

The gears framework in Marketing Cloud Personalization allows you to integrate
Personalization with other systems, take advantage of reusable templates, and
access the rich analytics data stored in Marketing Cloud Personalization. You
can enable or disable individual gears. For some gears, you can configure gear
settings in the UI.

  1. In the main navigation menu, hover over **Gears** and select **Gears**. 

The Installed Gears screen displays a list of installed gears, including its
name, a description, its status (enabled or disabled), and category.

  2. Navigate to the gear that you want to configure.

Gear Name | Description | Related Documentation  
---|---|---  
Account | Supports Account ETL feeds. | 
     * [Account ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_account_data_feed.htm&language=en_US&type=5 "Use the Account ETL data feed to update account information in Unified Account Profiles.")  
Campaign Stats Tracking | Tracks campaign statistics, including impressions, click-throughs, dismissals, and recommendations. Template requirements apply. | 
     * Developer Documentation: [Tracking Personalization Web Campaign Statistics](https://developer.salesforce.com/docs/marketing/personalization/guide/campaign-stats-tracking.html)  
Commerce | Supports Salesforce Commerce integration and associated ETL feeds. | 
     * [Product ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_product_data_feed.htm&language=en_US&type=5 "Use the Product ETL data feed to update the products in your catalog and to add new products.")
     * [Product Localization ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_product_localization_data_feed.htm&language=en_US&type=5 "Localize your catalog items based on language and country codes to display product information with the locale-specific data for each item. Used with the Product ETL data feed, the Product Localization ETL data feed enhances your catalog with a localized experience.")
     * [Transaction ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_transaction_data_feed.htm&language=en_US&type=5 "Use the Transaction ETL data feed to bulk upload transactions to associate purchases of items with individual user profiles.")  
Common | Supports various ETL feeds and associated configuration options. | 
     * [Catalog Object ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_catalog_object_data_feed.htm&language=en_US&type=5 "Use the Catalog Object ETL data feed to update articles, blog posts, and custom catalog objects.")
     * [Catalog Localization ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_catalog_localization_data_feed.htm&language=en_US&type=5 "Use the Catalog Localization ETL data feed to localize data for items in your catalog.")
     * [Category ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_category_data_feed.htm&language=en_US&type=5 "Use the Category ETL data feed to add categories to your catalog when creating your category hierarchies. You can update categories by uploading subsequent files that include existing category IDs. Categories are configured by default, but you can add attributes for them.")
     * [External Email Campaign Events ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_external_email_campaign_events_data_feed.htm&language=en_US&type=5 "You can use the External Email Campaign Events ETL data feed to import data from email campaigns that were sent by an external email service provider \(ESP\). Data can include sends, opens, and clicks.")
     * [Promotion ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_promotion_data_feed.htm&language=en_US&type=5 "Use the Promotion ETL data feed to add promotions for your catalog for both rule-based and machine learning-driven cross-channel decisioning.")
     * SegmentDelta ETL and SegmentReplace ETL (see [Create Manual Segments](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_manual.htm&language=en_US&type=5 "Manual segments consist of a fixed, specified list of users, as opposed to rule-based segments, whose users are determined in real time based on a defined set of criteria."))
     * [User ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5 "Use the User ETL data feed to update Unified Custom Profiles, and Unified Account Profiles if you have B2B Detect. Personalization stores user profiles for each anonymous and known user in the system.")  
Content Gear | Deprecated. Instead, for Article ETL and Blog ETL settings, use the Dimension ETL functionality in the Common Gear. | 
     * Refer to the Common gear settings.  
Corvus | Supports queries in the Corvus AI and returns Contextual Bandit results in a campaign template. | 
     * Developer Documentation: [Corvus AI](https://developer.salesforce.com/docs/marketing/personalization/guide/corvus-ai.html)  
Display Utilities | Provides capabilities for displaying templates based on user inactivity, exit intent, and scroll position. | 
     * Developer Documentation: [Web Template Display Utilities](https://developer.salesforce.com/docs/marketing/personalization/guide/web-template-display-utilities.html)  
Email | Supports email functionality, including subscriber-related ETLs feeds. | n/a  
Flicker Defender | Helps prevent flicker caused by the rendering of personalized content (templates/campaigns) served by the Marketing Cloud Personalization platform. | 
     * Developer Documentation: [Flicker Defender](https://developer.salesforce.com/docs/marketing/personalization/guide/flicker-defender.html)  
Handlebars Templates | Supports the rendering of handlebar templates built in the Visual Editor. | 
     * Developer Documentation: [Web Template Handlebars](https://developer.salesforce.com/docs/marketing/personalization/guide/web-template-handlebars.html)  
Hotel | Supports Hotel Gear components that are accessible to hotel clients. | 
     * [Hotel Gear Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear.htm&language=en_US&type=5 "The Hotel Gear is a data model you can use to feed data from your hotel booking systems into Marketing Cloud Personalization. You can use the data for segmentation, as well as for campaign and promotion targeting.")
     * [Activate the Hotel Gear](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_activate.htm&language=en_US&type=5 "Activate the Hotel Gear to bring in data from your hotel booking systems. The Hotel Gear is dataset-specific, so you must activate it for each dataset that has campaigns or promotions that you want to target with booking system data. You send booking system data by the Booking ETL data feed.")  
Journey Builder | Adds a user to Journey Builder on Segment Join. | 
     * [Export a Segment to Journey Builder](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_journey_builder.htm&language=en_US&type=5 "The Personalization system constantly gathers data about your users, your catalog, and other systems through channel events, API events, and data feeds to update segments in real time. Use segments to add users to journeys in Journey Builder within moments of the data changing as they join segments. Complete the following steps to export a segment to Journey Builder.")  
Journey Builder Action | Workflow Action that enters a user into a Journey. | 
     * [Configure a Triggered Campaign Template](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_save_global_template_dataset.htm&language=en_US&type=5 "A triggered template defines the data to pass to Journey Builder. You can modify it for each campaign experience, such as which recipe to show to the qualified user. To create a triggered campaign, you must have a triggered template in your dataset. Marketing Cloud Personalization includes a standard template that you can add fields to. If you need options other than what’s included in the default template, have your developer create a template.")  
Profile Objects | Supports Profile Object ETL feeds. | 
     * [User Profile Object ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_profile_object_data_feed.htm&language=en_US&type=5 "Use the User Profile Object ETL data feed to update the user profile objects you create.")  
Recommendations | Supports product or content recommendations using machine learning algorithms informed by real-time customer behavior, engagement, and context. | 
     * Developer Documentation: [Recommendations](https://developer.salesforce.com/docs/marketing/personalization/guide/recommendations.html?q=gear)  
Rules | Supports segment and campaign targeting rules, such as Action Count, User Attribute, Visit Count, and others. | 
     * [Segment Categories and Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_category_rule.htm&language=en_US&type=5 "Marketing Cloud Personalization provides various categories and accompanying rules for use with segments. When a user interacts with one of your channels, the Personalization system identifies the segments they belong to based on real-time session activity. Because segment updates happen in real time, membership changes occur immediately.")
     * [Rule Categories](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_rule.htm&language=en_US&type=5 "There are a variety of rules that you can add for campaign targeting and rule-based campaign experiences when you create or edit a campaign.")  
Salesforce CDP | Supports inbound activations from Salesforce Data Cloud. | 
     * [Data Cloud Activation ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_activation_data_feed.htm&language=en_US&type=5 "Use the Data Cloud Activation ETL data feed \(SalesforceCDPActivationETL\) to import user profile and segment data from Data Cloud into Marketing Cloud Personalization using Data Cloud’s Marketing Cloud Personalization Connector.")  
Segment File Exporter | Exports segment memberships. | 
     * [Export a Segment to the Personalization SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5 "Set up a nightly feed or a one-time export to synchronize segments with the Personalization SFTP. You can then use these segments in other systems to target cross-channel communications. For example, you can synchronize a segment to Marketing Cloud to target a specific group with an email communication.")
     * [Create a Segment Based on User Profile Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_create_user_profile.htm&language=en_US&type=5 "Use user profile attributes to create segments for your campaigns and target users based on those attributes.")
     * [Export a Segment to Marketing Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_marketing_cloud_steps.htm&language=en_US&type=5 "Set up a nightly feed or a one-time export to synchronize Personalization segments with Marketing Cloud. For example, you can synchronize a segment to Marketing Cloud to target a specific group with an email communication.")  
Surveys | Supports surveys for Web templates. | 
     * [Create a Survey](https://help.salesforce.com/s/articleView?id=sf.mc_pers_survey_create.htm&language=en_US&type=5 "Create a survey for a web campaign.")
     * Developer Documentation: [Web Surveys](https://developer.salesforce.com/docs/marketing/personalization/guide/web-surveys.html?q=gear)  
System Tools | Provides tools such as the Campaign Debugger. | 
     * Developer Documentation: [Campaign Debugger](https://developer.salesforce.com/docs/marketing/personalization/guide/campaign-debugger.html)  
Visual Editor | Supports the Visual Editor used to personalize Web Campaigns. | 
     * [Set Up the Visual Editor](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_visual_editor.htm&language=en_US&type=5 "Learn how to set up the Visual Editor.")  
  
  3. To change the gear status, click the gear name and, in the right panel, click **Enabled** or **Disabled**.
  4. Some gears have additional settings you can configure. To configure other gear settings, click the gear name and, in the right panel, click **CONFIGURE** , change any settings you want to update, and then click **SAVE**.

![de1c62de-e1c6-4e96-bba8-7ac2e1f3dbfb]

Note Changing a gear setting in the UI is a no-code way to influence gear
behavior. Configuring gears in the UI differs from customizing gears used in
campaign templates, which requires coding (as described in [Custom Interface
and Template
Configuration](https://developer.salesforce.com/docs/marketing/personalization/guide/custom-
interface-template-configuration.html)).

The following table describes configurable gear settings.  Gear Name | Configurable Fields  
---|---  
Account | 
     * **Account Etl Origin** —the channel over which Account ETLs are received  
Commerce | 
     * **Product Etl Origin** —the channel over which Product ETLs are received
     * **Product Etl Mark Excluded OOS** —Select to mark as zero (0) the inventory of all products in the catalog not in the file.
     * **Transaction Etl Sort Before Grouping** —Select to sort the data in the Transaction ETL before grouping.
     * **Transaction Etl Origin** —the channel over which Transaction ETLs are received
     * **Locale Product Etl Origin** —the channel over which Locale Product ETLs are received
     * **Locale Product Etl Sort Before Grouping** —Select to sort the data in the Locale Product ETL before grouping.  
Common | 
     * **User ETL Channel** —the channel for User ETLs
     * **Catalog Object ETL Channel** —the channel for Catalog Object ETLs
     * **Catalog Object Locale ETL Channel** —the channel for Catalog Object Locale ETLs
     * **Article ETL Channel** —the channel for Article ETLs
     * **Blog ETL Channel** —the channel for Blog ETLs
     * **Dimension ETL Channel** —the channel for Dimension ETLs
     * **Sort Dimensions Before Grouping** —Select to sort dimensions before grouping.
     * **Promotion ETL Channel** —the channel for Promotion ETLs
     * **Sort Promotions Before Grouping** —Select to sort promotions before grouping.
     * **External Campaign Event ETL Channel** —the channel for External Campaign Event ETLs
     * **Category ETL Channel** —the channel for Category ETLs
     * **Segment Delta ETL Channel** —the channel for Segment Delta ETLs
     * **Segment Replace ETL Channel** —the channel for Segment Replace ETLs  
Email | 
     * **Subscription List** —Select the subscription list for ETL processing. 
     * **Subscription List Replace Mode ('Replace' or 'Merge')** —Select whether to **Replace** or **Replace** subscription lists
     * **ETL Channel used for Subscriptions** —the ETL channel for subscriptions  
Hotel | 
     * **Booking Statuses** —Create status values for hotel bookings.
     * **Hotel Booking ETL Sort Before Grouping** —Select to sort data in the Hotel Booking ETL before grouping.
     * **Hotel Booking ETL Origin** —the channel over which Hotel Booking ETLs are received  
Profile Objects | 
     * **User Profile Object Etl Origin** —the channel over which User Profile Object ETLs are received  
Segment File Exporter | 
     * **Beta Segment Export** —Select to optimize the export of large segments.  
  

