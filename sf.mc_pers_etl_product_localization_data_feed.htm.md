

# Product Localization ETL Data Feed

Localize your catalog items based on language and country codes to display
product information with the locale-specific data for each item. Used with the
Product ETL data feed, the Product Localization ETL data feed enhances your
catalog with a localized experience.

## About Ingesting Product Localization Data

  * To use the Product Localization ETL data feed, enable the product localization feature on the Catalog Settings page.
  * Localization isn’t supported for custom attributes or related catalog objects. The schema shows which product attributes support localized values. 
  * If you include a product ID in the Product Localization ETL file that doesn’t exist in your catalog, Personalization creates the item. However, that item only has data for the locales that are included in the file. For example, if a dataset has an `en_US` configuration and you include a new item with only a locale of `fr_FR`, the item only displays data for the `fr_FR` locale. There isn’t any data to display for the en_US locale.
  * Datasets have a default language that you configure on the Catalog Settings page. This information is the locale for the catalog. To modify it, you must use the Product ETL data feed.

## Requirements

  * ETL files must be in a .csv file format that adheres to the schema for the data feed. Files that don’t follow the file naming conventions or the appropriate schema result in errors and fail to process.
  * Each row requires a product ID and a locale formatted as a two-letter lowercase ISO language code, an underscore, and a two-letter ISO uppercase country code.
  * Each product ID must have a single locale per row in the file, and all locale instances for a product must appear consecutively in the file. If a product ID appears multiple times in a file without being consecutive, the system only writes the last grouped instance of records for that product ID to the catalog. Personalization provides the ability to sort the Product Localization ETL file by product ID. Administrators can enable the sorting option on the Gear Configuration page.
  * Field names that begin with `attribute:` must match the custom attribute names in the Attributes section of the Catalog and Profile Objects > Products page. 

## Filename Format

`locale-product-YYYY-MM-DD_HH-MM-SS.csv`

## Schema

Field Name  | Description  | Example Values  | Maximum Length  | Sata Type   
---|---|---|---|---  
`id` | Required. Product IDs in the file must match the format of product IDs in the Personalization application and the site map, as well as the IDs in your Product ETL file.  | prod1237723 | 255 | String  
`locale` | Required. A five-character representation of the locale associated with the product. The format must be a two-letter lowercase ISO language code, an underscore, and a two-letter ISO uppercase country code. | en_USfr_FRde_DEen_AU | 5 | String  
`attribute:name` | Represents the name of a product, and must contain at least one alphanumeric character. | Slick New Kicks | 1023 | String  
`attribute:url` | An RFC-3986-compliant URL that represents the canonical product display page for the product. | https://example.com/products/prod1.html | 1023 | String  
`attribute:description` | Represents the description of the product, and must contain at least one alphanumeric character. | Some excellent new shoes | 250 | String  
`attribute:price` | The current offer price of the product to promote to users. Use a period as the decimal separator. Don't use thousands separators. | 19.99 | 1023 | Decimal/Float  
`attribute:currency` | An [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) currency code of three uppercase letters for the product. | USDAUDEUR | 3 | String  
`attribute:formattedPrice` | Represents the local price that displays to the user. | 6 Euros92 Canadian dollars | 255 | String  
  
## Sample File

id  | locale  | attribute:name  | attribute:url  | attribute:description  | attribute:price  | attribute:currency  | attribute:formattedPrice   
---|---|---|---|---|---|---|---  
prod007 | es_ES | El gorro | test.com/coche | Un gorro de lana para esquiar | 8 | EUR | 8 Euros  
31003 | fr_FR | Un chapeau | fr.com/chapeau | Un bonnet en laine pour le ski | 6 | EUR | 6 Euros  
31003 | en_AU | Hat | au.com/hat | A woolen hat for skiing | 9 | AUD | 9 Australian dollars  
99837 | en_AU | Boots | test.com/boots | Hiking boots | 99 | AUD | 99 Australian dollars  
99837 | fr_CA | Les bottes | test.com/bottes | Les bottes de randonnée | 92 | CAD | 92 Canadian dollars  
  
#### See Also

  * [ETL File Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_file_requirements.htm&language=en_US&type=5 "ETL files contain entries such as users, products, subscription list members, promotions, transactions, and more. These files must be in a CSV format and can be encrypted or compressed. The file formats must follow the explicit schema requirements for each ETL data feed. Typically, you upload ETL files automatically using the SFTP site, but you can also manually upload a file.")
  * [Monitor ETL Feed Jobs on the Feeds Dashboard](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_feeds_dashboard.htm&language=en_US&type=5 "The Feeds Dashboard provides details about ETL feed jobs.")

