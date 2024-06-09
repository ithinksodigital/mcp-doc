

# Built-In Identity Types

Identity types are specific identifiers that determine how Personalization
processes web events, API events, and channel events to identify users from
various sources. Personalization includes several built-in identity types,
such as email address and customer ID. The built-in identity types don’t
require configuration other than setting up event capture mechanisms, such as
the sitemap or ETL jobs.

These built-in identity types are available for the identity system to use for
identity lookup and merging user profiles:

![9089b428-b775-4e98-920a-13905adea567]

Note If the built-in identity types don’t meet the needs of your organization,
you can create three additional identity types.

Identity Type | Settings  
---|---  
Email Address | 

  * The **Uniqueness** parameter is set to **Identity Namespace** because each email address is unique to an individual in the identity namespace, which is the dataset. All user profiles with the same email address belong to the same individual, so Personalization can merge them.
  * The **Case-Sensitive** parameter is set to **False** because email addresses aren’t case-sensitive.

  
Profile ID | 

  * Profile ID is the identity type that Personalization uses for a unique Unified Customer Profile. All Unified Customer Profiles have an assigned profile ID.
  * The **Uniqueness** parameter is set to **Identity Namespace** because each profile ID is unique to an individual in the identity namespace, which is the dataset. 
  * The **Case-Sensitive** parameter is set to **False** because profile IDs aren't case-sensitive.

  
Salesforce CRM Lead ID | 

  * The **Uniqueness** parameter is set to **Identity Namespace** because each Salesforce CRM lead ID is unique to an individual in the identity namespace, which is the dataset. All user profiles with the same Salesforce CRM lead ID belong to the same individual, so Personalization can merge them.
  * The **Case-Sensitive** parameter is set to **True** because Salesforce CRM lead IDs are case-sensitive.

  
Salesforce CRM Contact ID | 

  * The **Uniqueness** parameter is set to **Identity Namespace** because each Salesforce CRM contact ID is unique to an individual in the identity namespace, which is the dataset. All user profiles with the same Salesforce CRM contact ID belong to the same individual, so Personalization can merge them.
  * The **Case-Sensitive** parameter is set to **True** because Salesforce CRM contact IDs are case-sensitive.

  
Customer ID | 

  * The **Uniqueness** parameter is set to **Identity Namespace** because a customer ID is unique to an individual in the identity namespace, which is the dataset. All user profiles with the same customer ID belong to the same individual, so Personalization can merge them.
  * The **Case-Sensitive** parameter is set to **False** because customer IDs aren’t case-sensitive.

  
Salesforce Marketing Cloud Contact Key | 

  * The **Uniqueness** parameter is set to **Identity Namespace** because each Salesforce Marketing Cloud contact key is unique to an individual in the identity namespace, which is the dataset. All user profiles with the same contact key belong to the same individual, so Personalization can merge them.
  * The **Case-Sensitive** parameter is set to **False** because Salesforce Marketing Cloud contact keys aren’t case-sensitive.

  
  
The Email Address, Salesforce Marketing Cloud Contact Key, and Customer ID
identity types already have corresponding user profile attributes. To use the
Salesforce CRM Lead ID and Salesforce CRM Contact ID identity types, follow
the steps in [Create a User Profile
Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_attributes_create.htm&language=en_US&type=5
"User profile attributes can collect data you can use in segmentation,
reporting, or with integrated third-party systems. For example, if you create
a form in Personalization, you can assign each field to an existing attribute.
Depending on the configuration of your dataset, the attributes can either
collect the data for reporting, or can write it to a third-party integrated
system.") to set up the associated attributes.

