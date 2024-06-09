

# ETL File Requirements

ETL files contain entries such as users, products, subscription list members,
promotions, transactions, and more. These files must be in a CSV format and
can be encrypted or compressed. The file formats must follow the explicit
schema requirements for each ETL data feed. Typically, you upload ETL files
automatically using the SFTP site, but you can also manually upload a file.

## File Naming and Extensions

  * All files must be in the RFC-4180 CSV file format. 
  * Character encoding must be UTF-8, and all maximum lengths are in UTF-8 encoded bytes.
  * ETL files can be compressed and encrypted. Valid compressed file extensions are .zip and .gz. The valid encryption extension is .pgp. 
  * Files don’t process unless the file names match the defined structure of the ETL data feed schemas. You can’t customize the schema of an ETL file.
  * Ensure that the file naming format is consistent for each data feed. Under most conditions, the ETL data feed name is followed by a date and time, such as `user-yyyy-mm-dd_hh-mm-ss.csv`. Marketing Cloud Personalization uses the date to process files in order when multiple files are uploaded at the same time. 
  * When sending files from Automation Studio for ETL processing, omit using minutes and seconds in file names. That is, when processing more than one file per day from Automation Studio, name files in the format `user-yyyy-mm-dd_hh.csv`. When processing only one file per day from Automation Studio, name files in the format `user-yyyy-mm-dd.csv`.

## File Header Structure

Files processed by built-in ETL components are handled consistently regardless
of the ETL type. Some data feed types have access to additional header
definitions because of the target data type, but fields generally fall into a
few different categories.

Field | Description  
---|---  
`id` | The ID of the item you’re uploading. There are instances when this header is named slightly differently, such as in the User ETL data feed.

  * ID values are case-sensitive. For example, “Shirt” and “shirt” represent two distinct items in the catalog.
  * ID values must not contain any spaces.

  
`categories` | This field is applicable only to the product, article, and blog post built-in catalog objects.  
`relatedCatalogObject` | The structure for handling related catalog objects in various ETL data feeds.  
`attribute` | The structure for handling system and custom attribute definitions. Personalization processes all fields that begin with `attribute:` as the attribute type defined in the schema or that you set when creating a custom attribute. When using a custom attribute, the value must be the unique defined name of the attribute, not the label used to display the attribute in Personalization. Custom date attributes are formatted as Unix epoch timestamps.  
  
## Frequency

The Personalization Gears system has a built-in listener for files on the SFTP
site. Every 15 minutes, each enabled ETL data feed checks the
`/dataset/inbound` directory for any files that match the expected filename
structure for that individual data feed. The general recommendation for file
processing frequency is daily. However, if you need files to process more
frequently, or you want to update stale data, consider uploading files hourly.
More frequent uploads ensure that the system has time to process files
completely, which prevents a file processing queue from forming.

## System Fields

Personalization has several built-in system fields to support attributes. The
system fields available for each type of ETL data feed vary, and have explicit
handling processes. Creating attributes with the same name as a system
attribute results in negative consequences for the data, such as when
including an item's name attribute in a Product ETL file. Although “name” is a
system field, Personalization reads from a “attribute:name” column header.
Creating a custom attribute called “name” for the Product catalog object on
the Catalog and Profile Objects page can have negative consequences during ETL
processing.

## Resetting Default Values

Except for the User ETL data feed, all ETL data feeds can reset field values
to their defaults (except where the field is required, such as an ID).
Resetting a value occurs when a record has an empty value for a column during
processing. Personalization treats the absence of a value as null, and removes
any existing values for that key on the record in Personalization. You can use
this process to remove an old description for an item, remove a custom
attribute for a transaction, or remove categories for a product.

Personalization expects that each record has a corresponding value for each
column, even in a delta file.

There are certain system fields whose unset values are slightly different than
an absent value. Some of these keys only apply to a subset of ETL types, but
are all listed in this table.

**Field Name** |  **Default Value**  
---|---  
`price` | 0  
`listPrice` | 0  
`rating` | 0  
`numRatings` | 0  
`inventoryCount` | 1 (the item is considered in stock)  
`published` | 1/1/1970  
`expiration` | Date of processing + 100 years (if it ran on 04/12/2022, the expiration date is 04/12/2122)  
`promotable` | True (the item is promotable)  
  
## Errors and Logging

  * If a column header doesn’t match an existing system field, custom attribute, or other valid column header in the schema for an ETL data feed, Personalization doesn’t upload those records. An error occurs when a column value doesn’t reflect valid data.
  * If you encounter an error that states "Warning: At least one Product is archived. Updates will not be visible in the UI," it means that at least one of the items in your ETL file is in an archived state. An item becomes archived when you include the `attribute:archived` column header of and a value of true in the ETL file, or when you click Delete next to the item in the catalog. To unarchive an item, confirm that the `attribute:archived` column is in your ETL file and the item has a value of false.
  * An error that states "extract failed most likely due to a column or line delimiter" indicates that a file has character mistakes, such as double quotes not closed, or extra commas throughout a value.
  * When errors occur for an ETL data feed, Personalization records each error message to the Logs dialog. The logs include the file line number that causes an error.
  * Personalization fails an ETL job when the error threshold reaches 10%. You can’t change the error threshold.
  * If a field in a record doesn’t map correctly to the data type indicated by its header, Personalization skips the record and doesn’t upload it. If there are enough instances of this type of error, Personalization fails the entire ETL file. 

## Feed Limits

For information about feed limits, see [Personalization
Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_limits.htm&language=en_US&type=5
"Learn about the limits and capabilities in Marketing Cloud
Personalization.").

## File Size Limits

For information about recommended file size limits, see [Personalization
Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_limits.htm&language=en_US&type=5
"Learn about the limits and capabilities in Marketing Cloud
Personalization.").

