

# Promotion ETL Data Feed

Use the Promotion ETL data feed to add promotions for your catalog for both
rule-based and machine learning-driven cross-channel decisioning.

## About Ingesting Promotion Data

To update or add an asset to an existing promotion, you must include all data
about the promotion in the ETL file, even if the values aren't changing. When
Personalization processes the ETL file, it replaces any existing data with the
data in the file.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Before uploading a promotion ETL data feed, confirm that promotions are enabled for your catalog. Also, be sure to add any applicable related catalog objects and attributes to the promotion.

![2167e34b-a83f-4351-abb2-5793449ac23a]

Note If the ETL file includes data associated with a related catalog object or
attribute that isn’t configured, Personalization doesn’t apply that data for
the promotion. Configure attributes and related catalog objects before
uploading the ETL file.

  * Sort the file by promotion ID. You can sort the file yourself before uploading it, or you can enable sorting on the Gear Configuration page by selecting the Promotion ETL Sort Before Grouping option. If the file isn't sorted, Personalization doesn’t upload it, so you must sort and resubmit the file to process it.

![cbe6b0ae-4e0e-4f7f-bde9-322f38565949]

Note If you aren’t sure of the ID for an existing promotion, select **Promotions** from the **Catalog** section of the main navigation, hover over a column header, click the three dots, and select **Columns** | **ID**.

  * To add multiple assets to a single promotion, include multiple lines with the same promotion ID. Each line item requires all promotion information, not just the asset details.
  * Field names that begin with `attribute:` must match the custom attribute names in the Attributes section of the Catalog and Profile Objects > Promotions page. 

## Example

If a promotion has three assets associated with it, you include the promotion
information in three rows in the ETL file. The only information that differs
for each row is the asset information.

  * If you’re updating a promotion, such as eligibility criteria, description, or URL, you must include all values associated with that promotion, even if each value isn’t changing.
  * When creating your promotion ETL file, remember that Personalization updates all columns (fields) that you include in the file, replacing existing data with the contents in the column’s rows. If a column row is blank, Personalization removes the existing data that maps to the blank row. If you don’t want to update or edit an existing value, don’t include the column for that value in your ETL file.
  * If you’re updating a promotion that has multiple assets, you must include a line item with that updated information for each asset. A promotion's assets are fully replaced with each ETL data feed, so only the assets in the most recent file exist for the promotion.

## Filename Format

`promotion-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

![ff3b5372-433c-4b9f-9e9d-4aba20440c76]

Note For a promotion to be eligible to use the Einstein Decisions web
template, you must include an asset with a contentZone or tag that matches one
of the web content zones defined in your site map.

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`id` | Required. Represents the unique identifier for a promotion. If a promotion exists with the ID of a promotion in the ETL file, Personalization updates it with the information in the file. | offer12345 | 255 | String  
`attribute:name` | Required. Represents the name of the promotion, and must contain at least one alphanumeric character. | Winter SavingsHuge Savings Event | 1023 | String  
`attribute:url` | Required. An RFC-3986-compliant URL that represents the destination to send the user to upon click. | https://example.com/default/footwear.html | 1023 | String  
`asset:imageUrl` | Required. A fully qualified URL for an assets image. You can only have one asset image link per row in the ETL file. If you’re associating multiple assets with a single promotion, you must have multiple rows for that promotion. Include all information pertinent to that promotion in each row, with the data for the assets being the only difference between each row. | https://example.com/img/shoes9876543.png | 1023 | String  
`asset:contentZones` | Required. Content zones and tags are eligibility filters applied to a promotion’s asset. A single asset can have multiple content zones or tags, which are referenced in a campaign to help filter the assets that return in a campaign response. Multiple content zones and tags can be added using a pipe-separated list. You can’t have duplicate content zones or tags on multiple assets that are tied to a single promotion. For example, if one promotion has two associated assets, they can’t share a common content zone or tag. They must be unique across those two assets.Content zones and tags can be duplicated across promotions. For example, if you have two promotions that each have one associated asset, they can both have the same content zone or tag. | Homepage Hero|Winter Savings|Spring Sale|Back to School | 1023 | String  
`attribute:published` | An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for the promotion’s published date. All dates are stored in UTC time. Timezone offsets aren’t supported. The promotion is available only to show to a user between the published and expiration dates. If you provide only a published date, a promotion becomes eligible to return in a campaign response on that date and remains eligible from that time forward. If you don’t provide any dates, a promotion always counts as an active promotion for campaign response consideration.  | 2022-04-12T10:23:37Z | 1023 | Date  
`attribute:expiration` | An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for the promotion’s expiration date. All dates are stored in UTC time. Timezone offsets aren’t supported. The promotion is available only to show to a user between the published and expiration dates. If you provide only an expiration date, a promotion becomes inactive on that date and is no longer eligible to return in a campaign response. If you don’t provide any dates, a promotion always counts as an active promotion for campaign response consideration.  | 2022-04-12T10:23:37Z | 1023 | Date  
`attribute:description` | Represents the description of the promotion, and must contain at least one alphanumeric character. | Great savings are here! | 250 | String  
`attribute:` | The custom attributes for the promotion. Column headers begin with `attribute:` and are followed by the attribute name as it appears on the Promotions page. The header value must match the attribute name in the system, and the values must conform to the configured data type. | attribute:loyaltyTierattribute:offerType | 1023 | Any (string, integer, Boolean, date)  
`relatedCatalogObject:` | You can define and import additional related catalog objects, such as brands, countries, destinations, and properties. Each related catalog object name must match a catalog object type configured on the Catalog and Profile Objects page. Column headers begin with `relatedCatalogObject:` and are followed by a catalog object name. When the related catalog object cardinality is "many per item,” a promotion can have multiple related catalog objects in separate columns, or multiple values for the same related catalog object separated by the pipe character in the same column. A literal pipe in one of the values is represented as two pipe characters in the file.Note: This field replaces the `dimension:` field.  | relatedCatalogObject:brandBrand1 | Brand2 | Brand 3relatedCatalogObject:destinationAmericarelatedCatalogObject:propertiesHotel1|Hotel2|Hotel3 | 255 | String  
`userMatchAttribute:[userAttributeName]` | Promotion eligibility criteria based on exact matches to user attributes can be included in the file. The user attribute must exist in the system for Personalization to apply the eligibility criteria to the promotion. A promotion can have multiple user attribute match criteria, which you add with multiple columns. The column header begins with `UserMatchAttribute:` and is followed by the name of the user attribute.Format the input for a user attribute as: “true” or “false” followed by a space and a pipe-separated list, such as `.false Salesforce|Tableau|Slack`. If the input begins with “true,” a user must have an attribute that matches at least one of the values in the subsequent pipe-separated list to qualify to receive the promotion in a campaign response. If the input begins with “false,” a user can’t have any attributes that match the values in the pipe-separated list to qualify to receive the promotion in a campaign response. | userMatchAttribute:loyaltyTiertrue 1|2|3userMatchAttribute:MobileAppDownloadfalse YuserMatchAttribute:Companyfalse Salesforce|Tableau|Slack | 1023 | Any (string, integer, Boolean, date)  
`exclusionSegments` | Represents promotion eligibility criteria based on segment exclusion logic. The segment IDs (not the segment names) in the file must exist in Personalization. To include multiple segment IDs, enter them as a pipe-separated list.See [Find a Segment’s ID](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_id_find.htm&language=en_US&type=5 "You use a segment’s ID when defining its automation process in Automation Studio. There are also instances when you need a segment’s ID for an ETL data feed.") for more information.If a user is a member of any of the segments listed in the segment exclusion criteria, they aren’t eligible to see the promotion.If a user is a member of segments listed in both the inclusion and exclusion criteria, the exclusion logic takes priority, and the user isn’t eligible to receive the promotion. | exclusionSegmentsgoXqo|ybkWF|MfYFa | 1023 | String  
`inclusionSegments` | Represents promotion eligibility criteria based on segment inclusion logic. The segment IDs (not the segment names) in the file must exist in Personalization. To include multiple segment IDs, enter them as a pipe-separated list.See [Find a Segment’s ID](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_id_find.htm&language=en_US&type=5 "You use a segment’s ID when defining its automation process in Automation Studio. There are also instances when you need a segment’s ID for an ETL data feed.") for more information.A user must be a member of all the segments listed in the inclusion criteria to be eligible to receive the promotion.If a user is a member of segments listed in both the inclusion and exclusion criteria, the exclusion logic takes priority, and the user isn’t eligible to receive the promotion. | inclusionSegmentsYqO7X|U5t0V|HToYr | 1023 | String  
`attribute:archived` | Indicates that this promotion is archived. When true, the item is not visible in the catalog.Defaults to false when no value is set. If this column is omitted from the feed file, then no changes will be made to the archived attribute. | FALSEfalseTRUEtrue | 1023 | Boolean  
  
## Sample File

id  | attribute:name  | attribute:url  | attribute:description  | attribute:published  | attribute:expiration  | asset:contentZones  | asset:imageUrl  | relatedCatalogObject:brand  | userMatchAttribute:loyaltyTier   
---|---|---|---|---|---|---|---|---|---  
offer1001 | 20% Off Shoes | https://www.northerntrailoutfitters.com/default/shoes | 20% offer on shoes | 2022-04-15 | 2022-05-01 | HomeHeroDesktop | https://www.northerntrailoutfitters.com/dw/image/v2/BDPX_PRD/on/demandware.static/-/Library-Sites-NTO-SFRASharedLibrary/default/dw3984b9da/images/category/footwear-category-1680-400.jpg |  |   
offer1001 | 20% Off Shoes | https://www.northerntrailoutfitters.com/default/shoes | 20% offer on shoes | 2022-04-15 | 2022-05-01 | HomeHeroMobile | https://www.northerntrailoutfitters.com/dw/image/v2/BDPX_PRD/on/demandware.static/-/Library-Sites-NTO-SFRASharedLibrary/default/dw9de36c8e/images/category/footwear-subcategory-men-200-200.png |  |   
offer1002 | Nutrition Promotion | https://www.northerntrailoutfitters.com/default/nutrition | Nutritional Promotion 2022 | 2022-05-10 | 2022-07-01 | HomeHeroDesktop|HomeHeroMobile | https://www.northerntrailoutfitters.com/dw/image/v2/BDPX_PRD/on/demandware.static/-/Library-Sites-NTO-SFRASharedLibrary/default/dwa91a0c16/images/category/nutrition-category-1680-400.jpg | Alpine | true Gold|Silver  
offer1003 | Electronics | https://www.northerntrailoutfitters.com/default/electronics | Electronics Promotion 2022 | 2022-06-01 | 2022-07-01 | HomeHeroDesktop | https://www.northerntrailoutfitters.com/dw/image/v2/BDPX_PRD/on/demandware.static/-/Library-Sites-NTO-SFRASharedLibrary/default/dw35e8ceb7/images/category/electronics-category-1680-400.jpg |  | false Bronze  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

