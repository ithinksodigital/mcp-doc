

# Connect to the Data Warehouse

Connect to your Marketing Cloud Personalization Data Warehouse from your BI
tool using the user account credentials, the JDBC or ODBC connection string,
and other connection settings. For example, you can explore personal data in
the Personalization Data Warehouse using Tableau, Marketing Cloud
Intelligence, or CRM Analytics.

![634994e5-b8b7-425b-a784-1236eceb4e15]

Note [](https://help.salesforce.com/s?language=en_US)The Data Warehouse is
available only for customers who have already purchased the Marketing Cloud
Personalization \- Data Warehouse add-on product.

## Use Your BI Tool to Connect

Use your favorite business intelligence (BI) tool to connect by JDBC or ODBC
to the Data Warehouse and explore its contents. After you’ve connected,
navigate the preformatted schema and explore the data. For information about
what’s available and how it’s structured, see the developer documentation in
[Data
Analytics](https://developer.salesforce.com/docs/marketing/personalization/guide/data-
analytics.htm).

## Encrypted Connections Only

The Data Warehouse requires SSL for all connections.

## Required Connection Information

Connect to the Data Warehouse using the information sent by email when the
user account was created. Most BI tools use either a JDBC or an ODBC
connection and require the following information:

  * Database name 
  * Username 
  * Password 
  * Host 
  * Port 
  * Schemas 

## Test the Connection

To verify the behavior you expect before proceeding to analyze the data, be
sure to test the connection. The Data Warehouse sets up scratch schema
automatically.

## Use a JDBC Connection

If you use the Data Warehouse with a BI tool that supports a JDBC connection,
use the sample JDBC Connection String.

Example: `jdbc:redshift://client-xxx.examplecluster.abc123xyz789.region-
xyz.amazonaws.com:5439/xxx`.

Replace the xxx placeholders with your own information. To test the
connection, use the string provided by email with your JDBC-connected BI tool.

## Use an ODBC Connection

If you use the Data Warehouse with a BI tool that supports an ODBC connection,
use the sample ODBC Connection String.

Example:

`Driver={Amazon Redshift (x64)};
Server=xxx.examplecluster.abc123xyz789.region-xyz.amazonaws.com; Database=xxx;
UID=xxx; PWD=insert_your_master_user_password_here; Port=5439`

Replace the xxx placeholders with your own information. For `Database=xxx`,
replace xxx with the value of the tenant name. To test the connection, use the
string provided by email with your ODBC-connected BI tool.

#### See Also

  * [Integrate Personalization with Tableau](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_tableau.htm&language=en_US&type=5 "In Tableau, connect to Marketing Cloud Personalization’s Data Warehouse and explore personalization data.")
  * [Integrate Personalization with CRM Analytics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crma.htm&language=en_US&type=5 "In Salesforce CRM Analytics, connect to Marketing Cloud Personalization’s Data Warehouse and explore personalization data. Import prediction scores from CRM Analytics into Personalization using ETL data feeds.")
  * [Integrate Personalization with Intelligence](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_marketing_cloud_intelligence.htm&language=en_US&type=5 "In Marketing Cloud Intelligence, explore personalization data in Marketing Cloud Personalization’s Data Warehouse. Marketing Cloud Intelligence supports advanced roll-up analysis and deeper media spend analytics.")

