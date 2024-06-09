# Campaign Development in Marketing Cloud Personalization

After implementing Marketing Cloud Personalization, developers need to shift
focus from data ingestion to cross-channel use case execution and enablement.
Along with being business user-friendly, Personalization's [Campaign &
Templates system](/docs/marketing/personalization/guide/web-campaigns-
templates.html) also empowers developers to determine what data and what level
of flexibility a business user has access to.

Personalization campaigns can be broken down into the following four types.

  * **Web Campaigns:** To support web campaigns, developers are responsible for integrating Personalization with the client's website (or websites) and developing web templates that business users can leverage to build out campaigns, including A/B/n and rules-based tests.

    * For information on integrating Personalization with your website, refer to the [Personalization Web Integration documentation](/docs/marketing/personalization/guide/web-integration.html).
    * For information on how to leverage campaign templates, refer to the [Web Templates documentation](/docs/marketing/personalization/guide/web-campaigns-templates.html).

  * **Server-Side Campaigns:** Developers can configure templates specifically for server-side campaigns by leveraging a similar approach as web campaigns. A business user can still control test configuration and setup but collaborates more closely with their development team to leverage Personalization's [Event API](/docs/marketing/personalization/guide/event-api.html) correctly for their campaign execution.

For information on building a Server-Side Campaign from a template, refer to
the [Server-Side Templates
documentation](/docs/marketing/personalization/guide/server-side-campaigns-
templates.html)

  * **Email Campaigns:** Although email campaigns are developed through the Personalization UI, they require some basic knowledge of HTML. Depending on the business users' capabilities, developers could have limited or no involvement in open-time email campaign development.

For information on configuring Open-time Email campaigns, see [Open Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign.htm)
on the Salesforce Help site.

  * **Mobile Campaigns:** Personalization can support campaigns for display on mobile devices by using responsive HTML (HTML5) in its standard web templates feature or through integration with native iOS and Android mobile apps.

For information on the Personalization Mobile SDK, refer to the
[Personalization Mobile Integrations
documentation](/docs/marketing/personalization/guide/mobile-integration.html).

  * [_Salesforce Help_ : Open Time Email Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign.htm)

