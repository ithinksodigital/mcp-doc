# The Personalization Sitemap

In traditional web development, a sitemap (or site map) is a hierarchical list
of pages of a website and the relationships between them. In Personalization,
a **Sitemap** represents the JavaScript configuration through which the
Personalization web-channel solution architecture is implemented. A
Personalization developer must configure a Sitemap to be able to collect the
user interactivity data on all desired website "page types" and support the
business requirements to:

  * Develop [web templates](/docs/marketing/personalization/guide/personalization-template-system.html) that enable the delivery of [web channel campaigns](/docs/marketing/personalization/guide/campaign-development.html) to targeted prospects and customers.
  * Enrich the company knowledge and data profiles of customers, prospects, products, and site content assets based on website visitor actions.
  * Enable the development of in-depth behavioral analytics and machine learning capabilities.

The JavaScript configured in a Personalization Sitemap provides the
functionality that enables Personalization to identify the following.

  * **User Profiles:** Identity, using a known user ID or anonymous user tracking ID, who interacts with the website, enabling user profile development based on browsing actions and existing data drawn from company systems.
  * **Page Types:** The type of page the user is browsing (Home page, Product page, and so on).
  * **Attributes:** Detailed data about the user's attributes and the business objects that the user is interacting with, such as product or service catalog items or other web content (blogs, articles, and so on).
  * **Content Zones:** Areas of each web page type that Personalization can monitor and target for personalized user engagement opportunities.
  * **Events:** Types of user activity to listen for that triggers events to Personalization.

Always remember to configure the JavaScript for a Personalization Sitemap
before developing Personalization [web
templates](/docs/marketing/personalization/guide/personalization-template-
system.html) that support customer engagement
[campaigns](/docs/marketing/personalization/guide/campaign-development.html)
based on customer and prospect web channel interactions.

For more information about any of the preceding topics, see:

  * [Capturing User and Account Attributes](/docs/marketing/personalization/guide/capturing-user-account-attributes.html)
  * [User Identity Mapping](/docs/marketing/personalization/guide/user-identity-mapping.html)
  * [Page Types](/docs/marketing/personalization/guide/page-types.html)
  * [Attributes](/docs/marketing/personalization/guide/attributes.html)
  * [Capturing User and Account Attributes](/docs/marketing/personalization/guide/capturing-user-account-attributes.html)
  * [Content Zones](/docs/marketing/personalization/guide/content-zones.html)

As part of the Personalization discovery process, a solution architect works
with the Personalization customer to understand the business context and
determine the web-channel solution architecture that the Sitemap configuration
needs to implement. The discovery process produces a **Sitemap Blueprint**
that provides the Sitemap developer with the following information.

  * **Site Catalog:** The brands, products, services, or other website content such as articles and blogs that Personalization needs to monitor. The site catalog also includes the specifications of product categories such as "home goods", "camping", and "winter wear", along with individual catalog objects such as color, gender, and keyword.
  * **Site Architecture:** The structure of the website and layout of page types. A large online retailer could have hundreds or even thousands of individual product pages, but the structural layout of each product page type is relatively similar. As a Sitemap developer, you must understand the website's architecture, and the types of pages that require configuration in the Sitemap.
  * **Attribute Model:** Attributes are used in a Sitemap to collect and store additional custom data for each relevant business object type. Business objects with associated attributes include users, accounts, catalog items, orders, and line items. Attributes can also include metadata on the attribute value, such as the attribute data origin/provider, sensitivity classification (PII, sensitive, non-sensitive), and the attribute value refresh date. Attributes provide additional information to Personalization that campaign developers can use for targeting, segmentation, and machine learning purposes. Part of the discovery process includes developing an attribute model schema that specifies the individual attribute name/value pairs, associated metadata, and the purpose of each attribute.
  * **Web Engagement Use Cases:** The Sitemap Blueprint specifies the use cases that explain how the business wants to engage with its prospects and customers through the website. The Sitemap Blueprint needs to include the website's [Content Zone](/docs/marketing/personalization/guide/content-zones.html) requirements.
  * **Site Events:** The types of actions performed by users on the website to be sent to Personalization for segmentation, campaign targeting, or behavioral tracking (machine learning). For more information on capturing events and sending them to Personalization via API, see [Sitemap Implementation](/docs/marketing/personalization/guide/sitemap-implementation.html) and [Event API](/docs/marketing/personalization/guide/event-api.html).

The Personalization Sitemap system is deployed by and executes within a Beacon
API and the Personalization module of the Salesforce Interactions SDK. A
Sitemap is integrated into a site by establishing a connection from the site
to Personalization through a `<script>` tag added in the site header, as shown
in the following example.

In the preceding example, `accountName` indicates your Personalization account
name and `instance` indicates your Personalization instance identifier. You
can retrieve these details by accessing **Gears** from the Personalization UI
and reviewing the URL. For example, if your Gears URL is
`https://demo.us-1.evergage.com/`, then your account name is `demo` and `us-1`
is your instance identifier.

The Sitemap is configured using the **Sitemap Editor** included with the
Personalization Visual Editor. After the Web SDK script tag has been added to
a site, you can use the Sitemap Editor to configure the site to support the
Personalization web channel solution. Using the Sitemap Editor, you can
leverage the JavaScript functions provided by the Personalization Web SDK
library and execute that functionality through HTTP requests to the
Personalization **Event API**.

Based on the validity and configuration of the Sitemap, HTTP requests are sent
automatically by the Web SDK. Additionally, the Web SDK provides a `sendEvent`
function in each namespace that can be called to send events through the
[Event API](/docs/marketing/personalization/guide/event-api.html).

For guidance on getting started with Personalization Site Mapping and the
Sitemap Editor, see [Getting Started with Site
Mapping](/docs/marketing/personalization/guide/sitemapping-getting-
started.html).

