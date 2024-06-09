

# How Personalization and Sales and Service Cloud Integration Works

Learn about how the integration works and how data is shared between Marketing
Cloud Personalization and Sales and Service Cloud.

DATA SHARED | Direction  | INTEGRATION TYPE | DATA SYNCHRONIZATION | How the Integration Works  
---|---|---|---|---  
Contacts, leads, and accounts | Bidirectional | Bidirectional API configured in third-party integrations | Nightly | 

  * Pushes to contacts and accounts
  * Pulls from leads, contacts, and accounts
  * Retrieves standard and custom fields for matched audiences
  * Updates Salesforce CRM with key personalization engagement data in custom fields

See [Integrate Personalization with Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm.htm&language=en_US&type=5
"Share data between Marketing Cloud Personalization and Salesforce CRM. Send
Personalization user and visitor information to Salesforce CRM. Receive CRM
data associated with text fields, dropdown menus, numeric values, or
segments.").  
Affinities component | From Personalization to Sales and Service Cloud | API from AppExchange | Real time | 

  * Lightning component
  * Managed package
  * Shows individual affinities from a defined time period on Sales and Service Cloud record pages

See [Add the Affinities Component to the Contact or Lead
Page](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_mgd_pkg_affinities_component_add.htm&language=en_US&type=5
"Add the Affinities component to view affinity data from Marketing Cloud
Personalization for a lead or contact.").  
Event Stream component | From Personalization to Sales and Service Cloud | API from AppExchange | Real time | 

  * Lightning component
  * Managed package
  * Shows what customers are doing in real time

See [Add the Customer Event Stream Component to a Contacts or Leads
Page](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_mgd_pkg_event_stream_add.htm&language=en_US&type=5
"Watch your customers interact with your business in real-time as well as view
historical activities right on a Contacts or Leads page with the event stream
component of the Personalization managed package. Events are based on the data
provided by the Interactions SDK or Sitemap. For custom events, you can view
event name, URL \(if applicable\), timestamp, and channel.").  
Next Best Promotion or Action  | From Personalization to Sales and Service Cloud | API from AppExchange | Real time | 

  * Lightning component
  * Managed package
  * Uses personalization server-side campaigns to define the next best promotion or action based on a user’s Unified Customer Profile

See [Server-Side
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign.htm&language=en_US&type=5
"Server-side campaigns integrate testing and personalization at the server-to-
server level. While Marketing Cloud Personalization handles the campaign
logic, you need a developer to write the code to call the appropriate APIs and
provide information about the website visitor.") and [Configure Server-Side
Campaigns for Next-Best-
Offers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_server_side_campaign_next_best_offers.htm&language=en_US&type=5
"To use the next-best offers component, you must configure server-side
campaigns in Marketing Cloud Personalization. A developer must create the
server-side template.").  
Next Best Recommendation | From Personalization to Sales and Service Cloud | API from AppExchange | Real time | 

  * Lightning component
  * Managed package
  * Uses personalization server-side campaigns to define the next best recommendation based on a user’s Unified Customer Profile

See [Server-Side
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign.htm&language=en_US&type=5
"Server-side campaigns integrate testing and personalization at the server-to-
server level. While Marketing Cloud Personalization handles the campaign
logic, you need a developer to write the code to call the appropriate APIs and
provide information about the website visitor.") and [Configure Server-Side
Campaigns for Next-Best-
Recommendations](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_connector_server_side_campaign_next_best_recommendations.htm&language=en_US&type=5
"To use the next-best recommendations component, you must configure server-
side campaigns in Marketing Cloud Personalization. A developer must create the
server-side template.").  
Personalization Action for Flows | From Sales and Service Cloud to Personalization | API from AppExchange | Real time | 

  * Managed package
  * Flows Apex Action Element
  * Sends Sales and Service record and field data to personalization in the form of identities, user attributes, and related profile objects

See [Automate Data Sent for Personalization Using
Flows](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_mgd_pkg_automate_data_w_flows.htm&language=en_US&type=5
"Automatically send data that is specific to a Named Individual Profile from
Sales or Service Cloud to Personalization.").  
  
#### See Also

  * [Sales to Service Cloud Use Cases](https://help.salesforce.com/s/articleView?id=sf.mc_pers_use_case_sales_service.htm&language=en_US&type=5)

