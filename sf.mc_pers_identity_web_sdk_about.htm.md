

# About Identity System Setup for the Salesforce Interactions SDK

Learn about setting up the identity system for the Marketing Cloud
Personalization module of the Salesforce Interactions SDK.

## Before You Configure

Before configuring Personalization’s identity system for the Salesforce
Interactions SDK, make sure to review this information:

  * [Identity Types and Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5 "Personalization’s identity system uses deterministic matching to create a Unified Customer Profile for each of your customers. Specific identifiers, called identity types, determine how to process web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. If the built-in identity types don’t meet the needs of your organization, you can create additional identity types.")
  * [Built-In Identity Types](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_built_in.htm&language=en_US&type=5 "Identity types are specific identifiers that determine how Personalization processes web events, API events, and channel events to identify users from various sources. Personalization includes several built-in identity types, such as email address and customer ID. The built-in identity types don’t require configuration other than setting up event capture mechanisms, such as the sitemap or ETL jobs.")
  * For details about updating your sitemap to include identity types and attributes, see the developer documentation at [Marketing Cloud Personalization Web Integration](https://developer.salesforce.com/docs/marketing/personalization/guide/web-integration.html?q=web%20integration).

## Identity Types in the Salesforce Interactions SDK

You can change the identity type that Personalization uses for identity lookup
and merging user profiles. For example, if you have email address and loyalty
ID as identity types, you can use loyalty ID instead of email address for
lookup and merge.

You use the selected identity type as the user.id parameter in your sitemap
for web events. You can include other identity types under the user.attributes
parameter. The supplied identity types accumulate in the web browser. If the
identity type for the user.id parameter changes, Personalization clears all
identity types on the client computer. The identity type for the user.id
parameter can change when a different person uses the browser on the same
device and logs in to a different account.

![41a6b9e3-e3be-40ab-a8fe-a3c022bd61d6]

Example

In this example, Salesforce Marketing Cloud contact key
(sfmcContactKeyFromPage) is the identity type for the web event, and it sends
as the user.id parameter. The web event also includes the email address
identity type as a user attribute.

    
    
    SalesforceInteractions.init({}).then(function(state) {
        const config = {
            global: {
                onActionEvent: (event) => {
                    if (sfmcContactKeyFromPage) {
                        event.user.id = sfmcContactKeyFromPage;
                    }
                    if (emailAddressFromPage) {
                        event.user.attributes = {
                            emailAddress: emailAddressFromPage
                        };
                    }
                }
            }
        };
    });

#### See Also

  * [ _Developer Documentation_ : Marketing Cloud Personalization Web Integration](https://developer.salesforce.com/docs/marketing/personalization/guide/web-integration.html)

