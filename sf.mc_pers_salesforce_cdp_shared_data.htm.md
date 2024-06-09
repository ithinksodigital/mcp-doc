

# Personalization Data Shared with Data Cloud

Marketing Cloud Personalization shares Unified Customer Profile, event, and
catalog data with Data Cloud.

## Unified Customer Profile Data

Marketing Cloud Personalization builds a Unified Customer Profile for each
known and anonymous user in real time. Personalization uses data it collects
with the Marketing Cloud Personalization module of the Salesforce Interactions
SDK, Mobile SDKs, real-time API events, and ETL data feeds. The Unified
Customer Profile can contain multiple identifiers for a user, as well as
contextual and demographic data, event data, cross-channel engagement data,
and affinities. Using the Data Cloud Connector, Personalization can share this
data with Data Cloud to enrich its user profiles.

Personalization shares the following Unified Customer Profile data with Data
Cloud:

  * System-defined identity attributes:
    * Profile ID
    * Email address
    * Customer ID
    * Salesforce Marketing Cloud contact key
  * Custom user profile attributes
  * System-defined anonymous profile flag

As users interact with various engagement channels, Personalization collects
data and places it in a real-time cache. Upon cache expiration,
Personalization sends the latest Unified Customer Profile data to Data Cloud.
Personalization sends all custom user attributes for a profile to Data Cloud
regardless of whether the attribute was included in the event payload.

Channel  | Shared Profile Data   
---|---  
Marketing Cloud Personalization module of the Salesforce Interactions SDK | Profile records and attributes are sent after a Salesforce Interactions SDK event.  
Mobile SDK | Profile records and attributes are sent after a Mobile SDK event.  
ETL Data Feeds | An ETL data feed for Data Cloud updates Profile records:

  * User ETL data feed
  * Transaction ETL data feed (only user attributes, no transaction data)
  * Manual Segment ETL data feed (only user attributes)

  
Event API | Profile records included in Event API calls are shared with Data Cloud.  
  
## Event Data

Personalization shares the following event data with Data Cloud:

  * Events that include an ItemAction value are passed to the Data Cloud [Catalog Event](https://developer.salesforce.com/docs/atlas.en-us.c360a_api.meta/c360a_api/c360a_api_engagement_mobile_sdk_catalog_event.htm), [Cart Event](https://developer.salesforce.com/docs/atlas.en-us.c360a_api.meta/c360a_api/c360a_api_engagement_mobile_sdk_cart_event.htm), or [Order Event](https://developer.salesforce.com/docs/atlas.en-us.c360a_api.meta/c360a_api/c360a_api_engagement_mobile_sdk_order_event.htm) object. Examples: View Item, Add to Cart
  * Events that include only an Action value are passed to the Data Cloud Base Event object. Examples: Search, Page View, Click

Personalization sends event data immediately after receiving an event.

Channel  | Shared Event Data  
---|---  
Marketing Cloud Personalization module of the Salesforce Interactions SDK | Events collected from the Salesforce Interactions SDK are sent to Data Cloud.  
Mobile SDK | Events collected from the Mobile SDK are sent to Data Cloud.  
ETL data feeds | Support for sending event data with an ETL data feed will be added in a future release.  
Event API | Events collected from the Event API are sent to Data Cloud.  
  
Mapping of ItemActions from Personalization objects within Data Cloud includes
the following:

Data Cloud Data Lake Object  | Personalization Item Actions  
---|---  
Catalog | 

  * View Item
  * View Item Detail
  * Quick View Item
  * View Item Out Of Stock
  * Stop Quick View Item
  * View Category
  * View Tag
  * Share
  * Review
  * Comment
  * Favorite

  
Cart | 

  * Add To Cart
  * Remove From Cart
  * View Cart
  * Update Line Item

  
Order | Purchase  
Base Event | Base events include events that feature only Actions, or ItemActions that don’t fit into the other three categories of this table. Examples include Home Page Visit and Email Signup.  
  
## Catalog Data

Personalization doesn’t share the full catalog with Data Cloud through the
Data Cloud Connector. To build a segment in Data Cloud based on a specific
ItemID from Personalization, use one of the following methods:

  * Reference the applicable ItemID (not Item Name) while defining your segmentation criteria.
  * Manually upload and map the catalog data from Personalization into the Data Cloud data model for reference in segment definition.

## Catalog Events

  * Dimension name from an event populates ItemType in the Data Cloud Catalog Event object.
  * ItemID from an event populates ItemID in the Data Cloud Catalog Event object.

