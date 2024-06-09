

# Category ETL Data Feed

Use the Category ETL data feed to add categories to your catalog when creating
your category hierarchies. You can update categories by uploading subsequent
files that include existing category IDs. Categories are configured by
default, but you can add attributes for them.

## About Ingesting Category Data

Categories support a hierarchy structure that allows individual categories to
have both parent and child categories. A category can have only one parent
category, but can have multiple child categories. Some example categories are
clothes, shirts, jackets, t-shirts, dress shirts, rain jackets, and winter
jackets.

Some examples of the full hierarchies are clothes>shirts>t-shirts,
clothes>shirts>dress shirts, clothes>jackets>rain jackets,
clothes>jackets>winter jackets. The Category ETL data feed creates these
relationships using the corresponding value of the attribute:parentCategoryId
field.

  * Each category must only appear in a single record in a file. Multiple records with the same ID cause errors, especially if they have different parent category IDs.
  * Personalization updates all columns (fields) that you include in the file, replacing existing data with the contents in the column’s rows. If a column row is blank, Personalization removes the existing data that maps to the blank row. If you don’t want to update or edit an existing value, don’t include the column for that value in your ETL file.
  * Category IDs on products, or any other catalog items in Personalization, must match the category IDs provided in the Category ETL file.
  * The Category ETL data feed doesn’t accept delta files. You must send the entire category structure in the file, regardless of whether each record in the file has changed. Personalization removes existing values from the catalog when a column contains blank values.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Field names that begin with `attribute:` must match the custom attribute names on the Attributes section of the Catalog and Profile Objects > Category page. 

## Filename Format

`category-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`id` | Required. Represents the identifier for the category. Category IDs must not contain any indication of hierarchy. The ETL file constructs the hierarchy for the catalog. | clothesshirtspantscat0001 | 255 | String  
`attribute:` | The custom attributes for the category. Column headers begin with `attribute:` and are followed by the attribute name as it appears on the Category page. The header value must match the attribute name in the system, and the values must conform to the configured data type. | attribute:commonNameAll Clothingattribute:sizelarge | 1023 | Any  
`attribute:parentCategoryId` | Recommended. The singular parent for a category ID. Root categories aren’t expected to have a parentCategoryId and instead are expected to have a value of true in the attribute:department column.Each ID must have a single parentCategoryId.Personalization uses parent category IDs to build an internal hierarchy. For example, a category of “slacks” with a parentCategoryId of “dress pants” that has a parentCategoryId of “pants” results in a hierarchy of pants|dress pants|slacks. The maximum hierarchy depth is 10 levels. | clothespantsshoes | 255 | String  
`attribute:department` | Represents whether a category is a top-level category. This value is false by default. | TrueFalse | 1023 | Boolean  
`attribute:name` | Represents the name of the category, and must contain at least one alphanumeric character. | Shoes | 1023 | String  
`attribute:url` | An RFC-3986 compliant URL that represents the canonical display page for the category. | https://example.com/products/cat1.html | 1023 | String  
`attribute:imageUrl` | Fully qualified URL for an image of the category. | https://example.com/img/img1.png | 1023 | String  
`attribute:description` | Represents the description of the category and must contain at least one alphanumeric character. | Men’s shoes | 250 | String  
`attribute:promotable` | This field defaults to true. When set to false, Personalization doesn’t return the product in the Einstein Recipes recommendation system.If no value is set, this field defaults to true. | TRUE | 1023 | Boolean  
`attribute:published` | An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for the category’s published date. Timezone offsets aren’t supported. | 2022-04-12T10:23:37Z | 1023 | Date  
`attribute:expiration` | An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for the category’s expiration date. Timezone offsets aren’t supported. | 2022-04-12T10:23:37Z | 1023 | Date  
`attribute:rating` | The rating value associated with the category. No specific scale is required, however, provide only the value. 9 is valid, 9/10 is invalid. | 4.5 | 1023 | Decimal/Float  
`attribute:numRatings` | The number of ratings associated with the category. | 57 | 1023 | Integer  
`attribute:archived` | Indicates whether the category is visible in the catalog. When true, the category isn’t visible. The default is false. If this column is omitted from the file, no changes are made to the attribute.If no value is set, this field defaults to false. | FALSEfalseTRUEtrue | 1023 | Boolean  
  
## Sample File

id  | attribute:parentCategoryId  | attribute:department  | attribute:name  | attribute:archived  | attribute:url  | attribute:imageUrl  | attribute:description  | attribute:promotable  | attribute:published  | attribute:expiration  | attribute:rating  | attribute:numRatings  | attribute:commonName   
---|---|---|---|---|---|---|---|---|---|---|---|---|---  
cat0001 |  | TRUE | Home | FALSE | test.com/c/home | test.com/c/home.jpeg | All Home Goods | TRUE | 2020-06-15 | 2100-01-01 | 5.0 | 5 | Home Goods  
cat002 |  | TRUE | Shoes | FALSE | test.com/c/shoes | test.com/c/shoes.jpeg | All Shoes | TRUE | 2020-06-15 | 2100-01-01 | 4.25 | 10 | Our Shoes  
cat003 |  | TRUE | Shirts | FALSE | test.com/c/shirts | test.com/c/shirts.jpeg | All Shirts | TRUE | 2020-06-15 | 2100-01-01 | 4.75 | 35 | Our Shirts  
cat004 |  | TRUE | Pants | FALSE | test.com/c/pants | test.com/c/pants.jpeg | All Pants | TRUE | 2020-06-15 | 2100-01-01 | 3.0 | 31 | Our Pants  
cat005 |  | TRUE | Hats | FALSE | test.com/c/hats | test.com/c/hats.jpeg | All Hats | TRUE | 2020-06-15 | 2100-01-01 | 3.0 | 11 | Our Hats  
cat006 |  | TRUE | Accessories | FALSE | test.com/c/accessories | test.com/c/accessories.jpeg | All Accessories | FALSE | 2020-06-15 | 2100-01-01 |  | 18 | Our Accessories  
cat0021 | cat002 |  | Sneakers | FALSE | test.com/c/home/shoes/sneakers | test.com/c/home/shoes/sneakers.jpeg | Sneakers for athletics, walking, running, and more | TRUE | 2020-06-15 |  |  |  | Our Sneakers  
cat0041 | cat004 |  | Slacks | FALSE | test.com/c/pants/slacks | test.com/c/pants/slacks.jpeg | Slacks for work and date night | TRUE | 2020-06-15 |  | 1.0 | 1 | Our Business Slacks  
cat0061 | cat006 |  | Watches | FALSE | test.com/c/accessories/watches | test.com/c/accessories/watches.jpeg | Our classic timepieces | TRUE | 2020-06-15 |  | 4.5 | 8 | Our Watches  
cat00211 | cat0021 |  | Running Sneakers | FALSE | test.com/c/shoes/sneakers/running-sneakers | test.com/c/shoes/sneakers/running-sneakers.jpeg | Sneakers for road races, trail races, track races and more | TRUE | 2020-06-15 |  | 4.0 | 6 | Our Trainers and Racers  
cat002111 | cat00211 |  | Racing Spikes | FALSE | test.com/c/shoes/sneakers/running-sneakers/racing-spikes | test.com/c/shoes/sneakers/running-sneakers/racing-spikes.jpeg | Shoes specifically for racing on tracks | TRUE | 2020-06-15 |  | 2.33 | 23 | Our Track and Field Spikes  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

