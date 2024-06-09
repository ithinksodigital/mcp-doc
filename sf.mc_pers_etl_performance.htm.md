

# ETL Ingestion Performance

Marketing Cloud Personalization doesn’t guarantee a throughput rate for ETL
ingestion, so it’s helpful to know which factors can affect ETL ingestion
rates. Many of these factors depend on the type of record that the feed
modifies. ETL processing speeds vary across accounts and datasets.

Each ETL feed in this topic lists the factors that affect the feed throughput,
starting with the factor with the highest impact.

## User ETL

  * The number of user profile documents to create or update
  * The size of the user profile documents to update, which includes the number of attributes, the change history, the visit history, the order history, the segment history, the profile objects, and daily statistics
  * The number of user attributes in the feed, along with the size of attribute values (for example, the length of strings)
  * The number of enabled segments in the dataset (and rules contained)
  * The number of identity attributes in the feed
  * The number of rows in the feed that interact with the same profile
  * The relative position of rows in the feed that interact with the same profile
  * The number of user profiles in the dataset

## Data Cloud Activation ETL

  * The size of the user profile documents to update, which includes the number of attributes, the change history, the visit history, the order history, the segment history, the profile objects, and daily statistics
  * The number of user attributes in the feed, along with the size of attribute values (for example, the length of strings)
  * The number of segments defined in the dataset (and rules contained)
  * When running in full replace mode, the number of users to remove from the segment (users previously in the segment but not included in the current feed)
  * When running in full replace mode, the number of users already in the segment that remain
  * The number of identity attributes in the feed
  * The number of rows in the feed that interact with the same profile
  * The relative position of rows in the feed that interact with the same profile
  * The number of user profiles in the dataset

## Account ETL

  * The number of accounts to create or update
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of enabled account segments in the dataset (and rules contained)

## Product ETL

  * The number of products to create or update
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of related catalog objects in the feed
  * The number of categories in the feed
  * The number of SKUs in the feed
  * The number of products in the dataset

## Product Localization ETL

  * The number of products to create or update
  * The number of locales in the feed
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of products in the dataset

## Transaction ETL

  * The number of orders in the feed
  * The number of line items in the feed
  * The number of user profiles to create or update
  * The size of the user profile documents to update, which includes the number of attributes, the change history, the visit history, the order history, the segment history, the profile objects, and daily statistics
  * The number of enabled segments in the dataset (and rules contained)
  * The number of identity attributes in the feed
  * The number of user profiles in the dataset

## Catalog Object ETL

  * The number of catalog objects to create or update
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of related catalog objects in the feed
  * The number of categories in the feed
  * The number of catalog objects in the dataset

## Catalog Object Locale ETL

  * The number of catalog objects to create or update
  * The number of locales in the feed
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of catalog objects in the dataset

## Category ETL

  * The number of categories to create or update
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of categories in the dataset

## External Email Campaign Event ETL

  * The number of user profiles to create or update
  * The size of the user profile documents to update, which includes the number of attributes, the change history, the visit history, the order history, the segment history, the profile objects, and daily statistics
  * The number of enabled segments in the dataset (and rules contained)
  * The number of identity attributes in the feed
  * The number of unique campaigns in the feed
  * The number of user profiles in the dataset

## Promotion ETL

  * The number of promotions to create or update
  * The number of attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of related catalog objects in the feed
  * The number of content zones in the feed
  * The number of user match attributes in the feed
  * The number of inclusion and exclusion segments in the feed
  * The number of promotions in the dataset

## Segment Delta ETL

  * The number of segment transitions in the feed
  * The number of user profiles to create or update
  * The number of identity attributes in the feed
  * The number of user profiles in the dataset

## Segment Replace ETL

  * The number of users to join the segment in the feed
  * The number of users to remove from the segment (user profiles previously in the segment but not included in the current feed)
  * When running in full replace mode, the number of users already in the segment that remain
  * The number of user profiles in the dataset

## User Profile Object ETL

  * The number of user profile documents to update
  * The size of the user profile documents to update, which includes the number of attributes, the change history, the visit history, the order history, the segment history, the profile objects, and daily statistics
  * The number of profile objects per user in the feed
  * The number of profile object attributes in the feed, along with the size of the attribute values (for example, the length of strings)
  * The number of related catalog objects in the feed
  * The number of enabled segments in the dataset (and rules contained)

#### See Also

  * [User ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_user_data_feed.htm&language=en_US&type=5 "Use the User ETL data feed to update Unified Custom Profiles, and Unified Account Profiles if you have B2B Detect. Personalization stores user profiles for each anonymous and known user in the system.")
  * [Data Cloud Activation ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_activation_data_feed.htm&language=en_US&type=5 "Use the Data Cloud Activation ETL data feed \(SalesforceCDPActivationETL\) to import user profile and segment data from Data Cloud into Marketing Cloud Personalization using Data Cloud’s Marketing Cloud Personalization Connector.")
  * [Available ETL Data Feeds](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_data_feed.htm&language=en_US&type=5 "Use these ETL data feeds for ETL integration.")

