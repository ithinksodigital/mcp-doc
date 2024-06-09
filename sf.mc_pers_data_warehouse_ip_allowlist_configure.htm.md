

# Configure the Data Warehouse IP Allowlist

Use the Data Warehouse IP Allowlist to improve system security and help
prevent unauthorized access to your Data Warehouse. Marketing Cloud
Personalization permits connections only from the IP ranges on the Allowlist.
If the Allowlist is empty, the Data Warehouse doesn’t accept connections from
any IP address.

### Required User Permissions

Permissions Needed  
---  
To create an IP Allowlist: | Administrator permissions  
  
![6a841daf-7a6e-4a13-95dd-03d99ba84392]

Note [](https://help.salesforce.com/s?language=en_US)The Data Warehouse is
available only for customers who have already purchased the Marketing Cloud
Personalization \- Data Warehouse add-on product.

Data Warehouse IP Allowlist rules apply to all datasets in an account.
Marketing Cloud Personalization supports only IPv4 and IPv6 ranges in CIDR
notation.

  1. From the main navigation menu, select **Security** | **Manage Data Warehouse.**
  2. Click the **Data Warehouse IP Allowlist** tab.
  3. To add an IP address or range, click **Add IP Range**.
  4. Enter an IPv4 or IPv6 range in CIDR notation.

For example: IPv4 range: 54.161.29.212/24, IPv6 range: 2001:db8:1234::/48

  5. Enter a short description for the IP range, such as “Office Network”.
  6. Save the entry. 

To delete an IP range, click the trash can icon.

![fa683492-3185-44a2-b240-a576e1987361]

Example

Specify a range of IP addresses that belongs to your office network. When
someone attempts to log in from outside your network, Data Warehouse denies
access to that person. An empty IP Allowlist blocks connections from all IP
addresses.

Previous

**[Create a Data Warehouse User
Account](https://help.salesforce.com/s/articleView?id=sf.mc_pers_data_warehouse_user_account_create.htm&language=en_US&type=5
"Access to the Data Warehouse requires authentication with a Data Warehouse
user account. After you create a user account, Marketing Cloud Personalization
sends an email with a JDBC and ODBC connection strings, along with other
information you need to connect to the Data Warehouse from your BI tool.")**

