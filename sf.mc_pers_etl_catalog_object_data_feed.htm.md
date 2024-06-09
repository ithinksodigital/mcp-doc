

# Catalog Object ETL Data Feed

Use the Catalog Object ETL data feed to update articles, blog posts, and
custom catalog objects.

## About Ingesting Catalog Data

Articles and blog posts are the only built-in catalog objects that you can
update with the Catalog Object ETL data feed. The other built-in catalog
objects—product, promotion, and category—each have their own ETL data feeds.

![1c36e1b4-e111-4fc3-b4c3-6fbd12f9d0d0]

Note The Catalog Object ETL data feed replaces the deprecated Dimension, Blog,
Article ETL data feed. Although the Dimension, Blog, Article ETL data feed is
functional, Salesforce recommends transitioning to the Catalog Object ETL data
feed.

The Catalog Object ETL data feed can’t create catalog objects. You must
configure the catalog objects before including them in the ETL file.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with `attribute:` must match the custom attribute names in the Attributes section of the Catalog and Profile Objects page for that catalog object. 

## Filename format

`catalog-object-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  |  Description  |  Example Values  |  Maximum Length  |  Data Type   
---|---|---|---|---  
`id` | Required. The unique identifier of the catalog object. If you’re updating the metadata for a catalog object captured via the site map, the ID must exactly match the ID in the site map. Personalization requires only a single instance of an ID in an ETL file. When an ID appears multiple times in the same file, the content of the last row with the ID overwrites any previous updates and uploads into the catalog. | brandName1brandName2brandName3brandName4 | 255 | String  
`catalogObjectType` | Required. This field must contain one of the catalog object types configured on the Catalog and Profile Objects page. | BrandArticle | 255 | String  
`attribute:<attribute name>` | The custom attributes for the catalog object. Column headers begin with `attribute:` and are followed by the attribute name as it appears in the Attributes section of the Catalog and Profile Objects page for the catalog object. | attribute:discountStatus | 1023 | Any  
`relatedCatalogObject:<catalog object name>` | Catalog objects can have related catalog objects. Each related catalog object name must match a catalog object type configured on the Catalog and Profile Objects page. Column headers begin with `relatedCatalogObject:` and are followed by a catalog object name. A catalog object can have multiple related catalog objects in separate columns, or multiple values for the same related catalog object separated by the pipe character in the same column. A literal pipe in one of the values is represented as two pipe characters in the file. | relatedCatalogObject:brandTier | 255 | String  
`attribute:name` | Represents the name of a catalog object, and must contain at least one alphanumeric character. | SaleRegular Price | 1023 | String  
`attribute:url` | An RFC-3986-compliant URL that represents the canonical product display page for the product. | https://example.com/brand.html | 1023 | String  
`attribute:imageUrl` | A fully qualified URL for an image of the catalog object. | https://example.com/img/brand.png | 1023 | String  
`attribute:description` | Represents the description of the catalog object, and must contain at least one alphanumeric character. | Products on Sale | 1023 | String  
`attribute:promotable` | This field defaults to true. When set to false, Personalization doesn’t return the product in the Einstein Recipes recommendation system.If no value is set, this field defaults to true. | TRUE | 1023 | Boolean  
`location:latitude` | The exact latitudinal value for the catalog object. Required if location:longitude is included.  | 43.641472 | 1023 | Decimal/Float  
`location:longitude` | The exact longitudinal value for the catalog object. Required if `location:longitude` is included.  | -70.240881 | 1023 | Decimal/Float  
`location:city` | Represents the name of the city, town, or village where the catalog object is located. | Boston | 1023 | String  
`location:state` | The state or region where the catalog object is located. In the US, use the two-letter postal abbreviation. | NYME | 2 | String  
`location:countryCode` | The [ISO 3166](https://www.iso.org/iso-3166-country-codes.html) alpha-2 country code where the catalog object is located. | US | 2 | String  
`location:postalCode` | Represents the postal code where the catalog object is located. | 04101 | 1023 | String  
`attribute:archived` | Indicates whether the catalog object is visible in the catalog. When true, the catalog object isn’t visible. The default is false. If this column is omitted from the file, no changes are made to the attribute.If no value is set, this field defaults to false. | FALSEfalseTRUEtrue | 1023 | Boolean  
  
## Sample File Structure: Update a single catalog object type

id  | catalogObjectType  | attribute:name  | attribute:url  | attribute:imageUrl  | attribute:description  | relatedCatalogObject:brandTier   
---|---|---|---|---|---|---  
brandName1 | Brand | Brand Name 1 | http://www.sample.com/brandName1 | http://www.sample.com/image/brandName1.jpg | really nice brand for athletic apparel | Standard  
brandName2 | Brand | Brand Name 2 | http://www.sample.com/brandName2 | http://www.sample.com/image/brandName2.jpg | Luxury brand for fancy occasions | Premium  
brandName3 | Brand | Brand Name 3 | http://www.sample.com/brandName3 | http://www.sample.com/image/brandName3.jpg | Imported luxury for the finest clothing items | Premium  
brandName4 | Brand | Brand Name 4 | http://www.sample.com/brandName4 | http://www.sample.com/image/brandName4.jpg | work wear for the toughest jobs | Standard  
  
## Sample File Structure: update multiple catalog object types

id  | catalogObjectType  | attribute:name  | attribute:url  | attribute:imageUrl  | attribute:description  |  attribute:published  |  attribute:rating  | attribute:numRatings  | relatedCatalogObject:brandTier  | categories  | relatedCatalogObject:Keywords   
---|---|---|---|---|---|---|---|---|---|---|---  
brandName1 | Brand | Brand Name 1 | http://www.sample.com/brandName1 | http://www.sample.com/image/brandName1.jpg | really nice brand for athletic apparel |  |  |  | Standard |  |   
brandName2 | Brand | Brand Name 2 | http://www.sample.com/brandName2 | http://www.sample.com/image/brandName2.jpg | Luxury brand for fancy occasions |  |  |  | Premium |  |   
brandName3 | Brand | Brand Name 3 | http://www.sample.com/brandName3 | http://www.sample.com/image/brandName3.jpg | Imported luxury for the finest clothing items |  |  |  | Premium |  |   
brandName4 | Brand | Brand Name 4 | http://www.sample.com/brandName4 | http://www.sample.com/image/brandName4.jpg | work wear for the toughest jobs |  |  |  | Standard |  |   
how-to-dress | Article | How to Dress | http://www.sample.com/how-to-dress | http://www.sample.com/summer-dress-image.jpg | Go-to guide for dressing this summer | 2022-03-15 | 4.5 | 78 |  | style guides | style|summer|fashion  
holiday-style | Article | Wow the Party this Holiday | http://www.sample.com/holiday-style | http://www.sample.com/holiday-scene.jpg | gear up to look good this holiday! | 2021-11-03 | 4.4 | 33 |  | style guides | style|holiday|fashion  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

