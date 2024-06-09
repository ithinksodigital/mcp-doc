

# Attribute Update Logic

You can use multiple sources to update attributes. Attributes retain values
from authenticated sources such as ETL or Channel: Server (/authevent API)
over lower priority sources, such as the web.

Attribute updates following an order of priority to determine which value to
retain.

  * Authenticated source

The ETL, Salesforce CRM integration, and channel Server in the authenticated
Event API (/authevent endpoint) are prioritized over unauthenticated sources
such as web, mobile, and non server-side events.

    * An attribute value sent in using an unauthenticated channel won’t overwrite the value set by a trusted channel. For example, an attribute value from ETL won’t be overwritten by an update from the web, even if the web attribute update has a more recent timestamp.
    * Trusted channels can overwrite each other. The timestamp is used to determine which attribute is kept when deciding between two values that are both from authenticated channels. For example, an attribute value set via Channel: Server can get overwritten by an attribute value provided by ETL (if the timestamp is more recent on the ETL attribute update).
  * Unauthenticated Sources

Unauthenticated sources are prioritized behind authenticated sources and won’t
update an attribute that has been set by an authenticated source. The
timestamp of the update determines the priority for all other sources, such as
web, mobile, and non-server-side event API updates.

#### See Also

  * [Create an Account Profile Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_account_profile_attributes_create.htm&language=en_US&type=5 "Account profile attributes can collect data you can use in segmentation, reporting, or with integrated third-party systems. For example, if you create a form in Personalization, you can assign each field to an existing attribute. Depending on the configuration of your dataset, the attributes can either collect the data for reporting, or can write it to a third-party integrated system.")
  * [Create a User Profile Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_attributes_create.htm&language=en_US&type=5 "User profile attributes can collect data you can use in segmentation, reporting, or with integrated third-party systems. For example, if you create a form in Personalization, you can assign each field to an existing attribute. Depending on the configuration of your dataset, the attributes can either collect the data for reporting, or can write it to a third-party integrated system.")

