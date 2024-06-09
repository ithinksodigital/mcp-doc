

# Create a Data Warehouse User Account

Access to the Data Warehouse requires authentication with a Data Warehouse
user account. After you create a user account, Marketing Cloud Personalization
sends an email with a JDBC and ODBC connection strings, along with other
information you need to connect to the Data Warehouse from your BI tool.

### Required User Permissions

Permissions Needed  
---  
To create a Data Warehouse user account: | Administrator permissions  
  
![f715c8b3-272f-4cfa-8e5c-49155862cb69]

Note The Data Warehouse is available only for customers who have already
purchased the Marketing Cloud Personalization - Data Warehouse add-on product.

  1. From the main navigation menu, select **Security** | **Manage Data Warehouse**.
  2. Click **Create Data Warehouse User**.
  3. Enter or select the **Data Warehouse Credentials** :

Field | Description  
---|---  
User Name | Enter the name of the user. User names must be lowercase, start with a letter or underscore character, and contain only alphanumeric values and allowed characters (, +, -, @, or .).  
Label | Specify a label for the account. The label is visible only on the **Manage Data Warehouse Users** screen.  
  
  4. Create a password.
  5. When prompted, be sure to save the user name and password in a secure location, in accordance with your company’s security policies.

![df451ebb-7a68-493c-a424-af3b0cecb808]

Important If you lose these credentials, you'll need to create a different
Data Warehouse user account to access the Data Warehouse.

  6. Click **Close**.

After you create a Data Warehouse user, Marketing Cloud Personalization sends
an email with a JDBC string, an ODBC string, and the additional information
required to make the connection. You can also see the connection string in the
**Connection String** field on the **Manage Data Warehouse Users** screen. The
Data Warehouse sets up the scratch schema automatically.

![2a9d52ca-4e3b-48a9-9b4b-80df9e3c0b7f]

Note The Data Warehouse requires SSL for all connections.

#### See Also

  * [ _Developer Documentation_ : Marketing Cloud Personalization Data Analytics](https://developer.salesforce.com/docs/marketing/personalization/guide/data-analytics.html)

Next

**[Configure the Data Warehouse IP
Allowlist](https://help.salesforce.com/s/articleView?id=sf.mc_pers_data_warehouse_ip_allowlist_configure.htm&language=en_US&type=5
"Use the Data Warehouse IP Allowlist to improve system security and help
prevent unauthorized access to your Data Warehouse. Marketing Cloud
Personalization permits connections only from the IP ranges on the Allowlist.
If the Allowlist is empty, the Data Warehouse doesn’t accept connections from
any IP address.")**

