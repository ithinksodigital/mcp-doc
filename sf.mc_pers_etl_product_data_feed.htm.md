

# Product ETL Data Feed

Use the Product ETL data feed to update the products in your catalog and to
add new products.

## About Ingesting Product Data

You can update existing products in your catalog by including updated records
with existing product IDs in the file. When you include records with new
product IDs, Personalization adds the new products to your catalog.

Product updates through an ETL data feed, or the Marketing Cloud
Personalization module of the Salesforce Interactions SDK, or the Event API,
don’t occur when a product is locked. A product becomes locked when you
manually edit the product's information and save changes. The assumption is
that a manual edit is intentional and takes precedence over any inbound data
source. While you edit a product page, the page appears as locked, and it
remains locked if you save the edits.

To determine whether a product is locked, select **Catalog** | **Products** from the main navigation, select the product, and look for the lock icon beside the product name in the details pane. If the product is locked, double-click it to edit it, select **Unlocked** from the dropdown at the top right, and click **Save**. Unlocking a product allows manual changes to be updated by ETL data feeds, the Marketing Cloud Personalization module of the Salesforce Interactions SDK, or the Event API.

## Requirements

  * ETL files must be in a CSV file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Each product must appear only one time in a single record in a file. If your file has multiple records with the same product ID, Personalization loads the last valid record in the file.
  * Location is a special type of catalog attribute available to products. To help denote where a product is located, information, such as geographic point (latitude and longitude), country code, city, and state, can be stored as system attributes. Location fields aren’t required, and only latitude and longitude are codependent. Any other combination of defined location fields is acceptable.
  * All records in the file, not just the records whose values have changed, need a value for each cell. Personalization overwrites existing values for any changed product records, including records that have blank values.
  * Field names that begin with `attribute:` must match the custom attribute names in the Attributes section of the **Catalog and Profile Objects** | **Products** page. 

## Filename Format

`product-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`id` | Required. Product IDs in the file must match the format of product IDs in the Personalization application and the site map. Ensure there's a single occurrence of an ID in the file. When multiples of the same product IDs exist in the file, Personalization loads only the contents of the last row to the catalog. This field is also the parent identifier of SKUs.  | prod1237723 | 255 | String  
`attribute:<attribute name>` | The custom attributes for the product. Column headers begin with `attribute:` and are followed by the attribute name as it appears on the Products page. The header value must match the attribute name in the system, and the values must conform to the configured data type. | attribute:fitwideattribute:lengthlong | 1023 | Any  
`relatedCatalogObject:<catalog object name>` | Each related catalog object name must match a catalog object type configured on the Catalog and Profile Objects page. Column headers begin with “relatedCatalogObject:” followed by a catalog object name. A product can have multiple related catalog objects in separate columns, or multiple values for the same related catalog object separated by the pipe character in the same column. A literal pipe in one of the values is represented as two pipe characters in the file.This field replaces the dimension: field.  | relatedCatalogObject:ColorBlue|YellowrelatedCatalogObject:MaterialLeather | 255 | String  
`categories` | Define multiple categories using pipe delimiting. | Footwear | RunningMen | Footwear | RunningWomen | Footwear | Running | 255 | String  
`skus` | The set of SKUs for the product, separated by a pipe character. A literal pipe in one of the values is represented as two pipe characters in the file. SKUs are case-sensitive. This field is typically used when all SKUs share the same product information. | sku104272|sku32342|sku33388 | 255 | String  
`attribute:name` | Represents the name of the product, and must contain at least one alphanumeric character. | Slick New Kicks | 1023 | String  
`attribute:url` | An RFC-3986-compliant URL that represents the canonical product display page for the product. | https://example.com/products/prod1.html | 1023 | String  
`attribute:imageUrl` | A fully qualified URL for an image of the product. | https://example.com/img/img1.png | 1023 | String  
`attribute:description` | Represents the description of the product, and must contain at least one alphanumeric character. | Durable and breathable, high-performing shoes for progressive explorers. | 250 | String  
`attribute:promotable` | This field defaults to true. When set to false, Personalization doesn’t return the product in the Einstein Recipes recommendation system.If no value is set, this field defaults to true. | TRUE | 1023 | Boolean  
`attribute:price` | The current offer price of the product to promote to users. Use a period as the decimal separator. Don't use thousands separators. | 19.99 | 1023 | Decimal/Float  
`attribute:listPrice` | A list price or MSRP to illustrate the savings when compared with the price. Use a period as the decimal separator. Don't use thousands separators. | 25.00 | 1023 | Decimal/Float  
`attribute:priceDescription` | Descriptive text for the price. | On sale this week only | 1023 | String  
`attribute:margin` | The profit margin of the product. The sale price minus the current cost of goods. Use a period as the decimal separator. Don't use thousands separators. | 2.451000.67 | 1023 | String  
`attribute:inventoryCount` | A count of product inventory. 0 count is considered out-of-stock and isn’t promotable in product recommendations. If this value is omitted, the field defaults to in-stock (1). | 30 | 1023 | Integer  
`attribute:published` | An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for the product’s published date. Timezone offsets aren’t supported. | 2022-04-12T10:23:37Z | 1023 | Date  
`attribute:expiration` | An [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) date and time string for the product’s expiration date. Timezone offsets aren’t supported. | 2022-04-12T10:23:37Z | 1023 | Date  
`attribute:currency` | An [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) currency code of three uppercase letters for the product. | USDAUDEUR | 3 | String  
`attribute:rating` | The rating value associated with the product. No specific scale is required, however, provide only the value. 9 is valid, 9/10 is invalid. | 4.5 | 1023 | Decimal/Float  
`attribute:numRatings` | The number of ratings associated with the product. | 57 | 1023 | Integer  
`location:latitude` | The exact latitudinal value for the product. Required if location:longitude is included.  | 43.641472 | 1023 | Decimal/Float  
`location:longitude` | The exact longitudinal value for the product. Required if location:latitude is included.  | -70.240881 | 1023 | Decimal/Float  
`location:city` | Represents the name of the city, town, or village where the product is located. | Boston | 1023 | String  
`location:state` | The state or region where the product is located. In the US, use the two-letter postal abbreviation. | NYME | 2 | String  
`location:countryCode` | The [ISO 3166](https://www.iso.org/iso-3166-country-codes.html) alpha-2 country code where the product is located. | US | 2 | String  
`location:postalCode` | Represents the postal code where the product is located. | 04101 | 1023 | String  
`attribute:archived` | Indicates whether the product is visible in the catalog. When true, the product isn’t visible. The default is false. If this column is omitted from the file, no changes are made to the attribute.If no value is set, this field defaults to false. | FALSEfalseTRUEtrue | 1023 | Boolean  
  
## Sample File

id  | attribute:name  | attribute:archived  | attribute:url  | attribute:imageUrl  | attribute:price  | attribute:listPrice  | attribute:inventoryCount  | attribute:description  | attribute:currency  | attribute:formattedPrice  | relatedCatalogObject:SaleStatus  | relatedCatalogObject:Gender  | categories  | skus   
---|---|---|---|---|---|---|---|---|---|---|---|---|---|---  
prod001 | Glasses | FALSE | http://www.sample.com/products/product001 | http://www.sample.com/image/product001.jpg | 100.12 | 100.12 | 1 | Glasses made to block blinding light | USD | Now $100.12 | OnSale | Men | Clothing|Outerwear | sku1000|sku1001|sku1002  
prod002 | Jacket | FALSE | http://www.sample.com/products/product002 | http://www.sample.com/image/product002.jpg | 54.63 | 59 | 1 | A black leather jacket | USD |  | OnSale | Men|Women|Unisex | Clothing|Outerwear|Leather |   
prod003 | Shirt | FALSE | http://www.sample.com/products/product003 | http://www.sample.com/image/product003.jpg | 10 |  | 1 | A blue polo shirt | AUD | Now $10 |  | Unisex | Clothing|Shirt | sku2000|sku2002|sku2004  
prod004 | Shorts | FALSE | http://www.sample.com/products/product004 | http://www.sample.com/image/product004.jpg | 33 | 60 | 1 | Beige khaki shorts | EUR | Now €33 | OnSale | Men | Clothing|Pants|Shorts | sku300|sku301|sku302|sku399  
prod005 | Pants | FALSE | http://www.sample.com/products/product005 | http://www.sample.com/image/product005.jpg | 99.98 | 120 | 0 | Blue jeans | USD | Now $99.98 | ClosingSale | Men | Clothing|Pants | sku401|sku403|sku411  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

