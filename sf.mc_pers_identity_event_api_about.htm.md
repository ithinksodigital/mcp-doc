

# About Identity Setup for the Event API

Learn about setting up the identity system for the Event API.

## Before You Configure

Before configuring Personalization’s identity system for the Event API, make
sure to review this information:

  * [Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5 "Personalization’s identity system uses deterministic matching to create a Unified Customer Profile for each of your customers. Specific identifiers, called identity types, determine how to process web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. If the built-in identity types don’t meet the needs of your organization, you can create additional identity types.")
  * [Built-In Identity Types](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_built_in.htm&language=en_US&type=5 "Identity types are specific identifiers that determine how Personalization processes web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. The built-in identity types don’t require configuration other than setting up event capture mechanisms, such as the sitemap or ETL jobs.")

## API Request Format

For information about formatting API requests, see the developer documentation
for [Event API
Requests](https://developer.salesforce.com/docs/marketing/personalization/guide/event-
api.html).

![4d4b2865-d9d4-46aa-b5d8-9703bfafc19a]

Example

**Option A**

In the following example, the API request sends the email address and customer
ID identity types as user attributes. The request doesn’t include the user ID
parameter.

    
    
    {
        "action": "sample",
        "user": {
            "attributes": {
                "emailAddress": "test@test.com",
                "CustomerId": "123"}
            },
        "source": {
                "channel": "Server",
        }
    }
    

**Option B**

In the following code example, customer ID is the identity type for the event
API, and the API request is sending it as the user ID parameter. The API
request also includes the email address identity type as a user attribute.

    
    
    {
        "action": "sample",
        "user": {
            "id": "456",
            "attributes": {
                "emailAddress": "test@test.com"}
            },
        "source": {
                "channel": "Server",
       }
    }
    

