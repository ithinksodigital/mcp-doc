

# Catalog Localization ETL Data Feed

Use the Catalog Localization ETL data feed to localize data for items in your
catalog.

## About Ingesting Catalog Localization Data

Personalization supports the localization of catalog items, which allows
unique data for specific fields to be stored based on the language and country
codes. The locale-specific data can then be leveraged on site (provided you
are tracking users' locale information on your website using the sitemap) to
display catalog object information with the locale-specific data for the
catalog item.

The Catalog Object Locale ETL allows for the ingestion of locale-specific
catalog object information for Articles, Blogs, and any user-created catalog
object. Promotions do not support localized attributes. The Catalog Object
Locale ETL should be used in conjunction with a Catalog Object ETL or another
method of populating catalog object items in the catalog.

## Ingestion Considerations

  * The Catalog object localization setting on the Catalog and Profile Objects settings screen must be turned on for the Catalog Object Locale ETL to function.
  * Only certain catalog object attributes support localized values (Name, Description, URL).
  * Localization is not supported for custom attributes or related catalog objects.
  * If an item is included in the Catalog Object Locale ETL, but does not exist in the Personalization catalog before ingesting the file, an item with the source ID will be created. However, that item will only have the data in locales which are included in the file. For example, if a dataset is in the default configuration (`en_US`) and a new item with only a locale of `fr_FR` is included, the item will only load data to the `fr_FR` locale – there will not be any data in the `en_US` locale.
  * Multiple catalog object types can be included in a single file.
  * Datasets have a default language in Personalization - this is configured in the Catalog Object Setup screen (see [Catalog Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object.htm&language=en_US&type=5 "Catalog objects and their relationships define the structure of your catalog. Personalization uses catalog objects to interpret and understand customer engagement and affinities. Examples of catalog objects include products, articles, blog posts, categories, brands, styles, and features. Personalization includes several built-in catalog objects, and you can create custom ones to meet your specific needs.")). This information is considered the default locale of the catalog and should be updated by the standard Catalog Object ETL. 

## Requirements

  * Each row requires a catalog object item ID and a locale in the format of "2-letter lower-cased language code", "underscore", "2-letter upper-cased country code". Examples: `en_US`, `fr_FR`, `de_DE`, `en_AU`, and so on. 
  * Each catalog object item should have a single locale per row of the file. Every locale instance of a catalog object item should appear consecutively in the file.
  * The Catalog Object Locale ETL file needs to be sorted by catalog object type so that all catalog objects of the same type appear in consecutive rows. Sorting can be achieved by the client prior to loading the file into the system.
  * Supported locales are visible in the platform via the locale drop-down on the Catalog and Profile Objects Settings screen (**Settings > Catalog and Profile Objects**). 

## Filename Format

`locale-catalog-object-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  |  Minimum Requirements  |  Example Values  |  Max Length  |  Personalization Data Type   
---|---|---|---|---  
`id` | Required. Catalog Object IDs must exactly match the catalog object IDs provided on site and captured by Personalization site mapping, as well as IDs provided in your Catalog Object ETL. | brand123 | 255 | String  
`catalogObjectType` | Required. Catalog Object Type must match one of the catalog object types configured on the Catalog and Profile Objects (see [Catalogs, User Profile Objects, and Promotions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_profile.htm&language=en_US&type=5 "Catalogs are collections of organized and related items that customers can purchase, view, or interact with.")). It should match the name value of the object type, not the label value. | Brand |  |   
`locale` | Required. A 5-character representation of the locale associated with the catalog object item information in the row. The structure of which must be "2-letter lowercased language code", "underscore", "2-letter uppercased country code". | en_US, fr_FR, de_DE, en_AU | 5 | String  
System Fields |  |  |  |   
`attribute:name` | Represents the name of a catalog object. Must contain at least one alphanumeric character. | Zapatos | 1023 | String  
`attribute:url` | RFC-3986. Complete URLs that represent the display page for this catalog object. | https://example.com/categories/zapatos.html | 1023 | String  
`attribute:description` | Represents the description of the product. Must contain at least one alphanumeric character to be set. | zapatos geniales | 250 | String  
  
## Sample File

id  | catalogObjectType  | locale  | attribute:name  |  attribute:url  | attribute:description   
---|---|---|---|---|---  
Brand001  |  Brand  |  es_ES  |  Brand Name 1  |  http://www.sample.com/brandName1  |  Really nice brand for athletic apparel   
Brand002  |  Brand  |  es_ES  |  Brand Name 2  |  http://www.sample.com/brandName2  |  Luxury brand for fancy occasions   
Brand003  |  Brand  |  fr_US  |  Brand Name 3  |  http://www.sample.com/brandName3  |  Comfortable work-wear for the toughest jobs   
BlogPost001  |  Blog  |  kr_KR  |  Blog Post Name 1  |  http://www.sample.com/BlogPost1  |  Impact of remote work in the work place   
Article001  |  Article  |  en_AU  |  Article Name 1  |  http://www.sample.com/Article1  |  Go-to guide for what luxury looks like in the modern age   
Article002  |  Article  |  en_AU  |  Article Name 2  |  http://www.sample.com/Article2  |  How to dress up athletic wear for your work from home meetings.   
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

