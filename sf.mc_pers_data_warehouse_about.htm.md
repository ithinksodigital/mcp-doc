

# About the Data Warehouse

Learn about the Marketing Cloud Personalization Data Warehouse.

![af766a84-119f-48c4-9d43-5030ab251104]

Note [](https://help.salesforce.com/s?language=en_US)The Data Warehouse is
available only for customers who have already purchased the Marketing Cloud
Personalization \- Data Warehouse add-on product.

## Data Warehouse Environment

The Marketing Cloud Personalization Data Warehouse environment includes:

  * Named users, datasets, and segments you specify 

For information about Data Warehouse limits, see [Personalization
Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_limits.htm&language=en_US&type=5
"Learn about the limits and capabilities in Marketing Cloud
Personalization.").

  * A connection string
  * Database schema, as specified in the developer documentation at [Data Warehouse](https://developer.salesforce.com/docs/marketing/personalization/guide/data-warehouse.html))
  * An AWS Redshift database
  * Login information

## Data Warehouse Updates

Marketing Cloud Personalization provides daily updates from the operational
data store to the Data Warehouse. Data Warehouse imports are based on the most
recent activity timestamp and order update time. Records updated by User ETL
transfer only when there’s user activity or when you load orders.

#### See Also

  * [ _Developer Documentation_ : Data Warehouse](https://developer.salesforce.com/docs/marketing/personalization/guide/data-warehouse.html)
  * [ _Developer Documentation_ : Data Dictionary](https://developer.salesforce.com/docs/marketing/personalization/guide/data-dictionary.html)
  * [ _Developer Documentation_ : Scratch Schema](https://developer.salesforce.com/docs/marketing/personalization/guide/scratch-schema.html)

