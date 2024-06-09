

# Personalization Limits

Learn about the limits and capabilities in Marketing Cloud Personalization.

## Datasets Limit

A Personalization account has a maximum of 20 datasets.

## Data and Object Limits (All Editions)

Marketing Cloud Personalization specifies the following limits for objects
within a dataset.

Catalog Object Limits

Marketing Cloud Personalization imposes limits per dataset for catalog objects
and attributes. For more information, see [Catalog
Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object.htm&language=en_US&type=5
"Catalog objects and their relationships define the structure of your catalog.
Personalization uses catalog objects to interpret and understand customer
engagement and affinities. Examples of catalog objects include products,
articles, blog posts, categories, brands, styles, and features.
Personalization includes several built-in catalog objects, and you can create
custom ones to meet your specific needs.").

Number of  | Limit  | Description   
---|---|---  
Active items per catalog object type | 2 million | An active item is one that is eligible for recommendations.Examples: 2 million products, 2 million brands, 2 million articles, or 2 million blog posts  
Total items across all catalog object types | 10 million | This limit is the total for all catalog objects.  
Custom catalog object types | 25 | This limit is for user-created catalog object types. This limit doesn’t count the built-in catalog objects (Product, Blog, Article, Promotions, and Category).Examples: brand, style, tags, keywords, author, color  
Attributes for a catalog object (built-in attributes + user-created attributes)This limit includes the following built-in attributes, which differ slightly for some of the built-in catalog objects: | 35 |   
  
  * products

| 16 | Product built-in attributes: (id, name, url, description, published, expiration, rating, numRatings, imageUrl, promotable, price, listPrice, priceDescription, currency, inventoryCount, margin)  
  
  * blogs

| 10 | Blog posts built-in attributes: (id, name, url, description, published, expiration, rating, numRatings, imageUrl, promotable)  
  
  * articles

| 10 | Article built-in attributes: (id, name, url, description, published, expiration, rating, numRatings, imageUrl, promotable)  
  
  * custom catalog objects

| 10 | User-created catalog object built-in attributes: (id, name, url, description, published, expiration, rating, numRatings, imageUrl, promotable)  
Related catalog object values for a single item | 50 | You can store up to 2 million of each catalog object type. When you create a catalog object relationship, you can store up to 50 values on the item.Example: Suppose your primary catalog object is a hotel that has a related catalog object named Amenity (representing amenities such as free wifi, a pool, gym, room service, bar). You can assign up to 50 amenity tags to that related catalog object. You can have more than 50 amenity values stored in Marketing Cloud Personalization (up to 2 million), but only 50 of those values can be stored against a single item.  
Category values for a single item | 15 | Personalization automatically applies the category object as a related catalog object to the built-in objects (products, blogs, articles).Example: A hierarchy (such as Men’s|Clothing|Tops|Shirts) is a single category value.  
  
Promotion and Asset Limits

Marketing Cloud Personalization specifies limits per dataset for promotions,
segments, and assets. For more information, see [Campaign
Promotions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion.htm&language=en_US&type=5
"Offer your customers special deals or advertise specific products with
campaign promotions in Marketing Cloud Personalization. A promotion is an
image that encourages customers to click through for more details. You can
deploy promotion images on a web page or in an email, including call-to-action
messages or incentives to engage customers and achieve specific business
goals. You can also use promotions with Einstein Decisions for rule-based
decisions and machine learning to target customers in multiple channels.").

Number of  | Limit | Description  
---|---|---  
Active promotions | 10,000 | An active promotion is any promotion eligible for a campaign to return. See the Einstein Decisions limit below, “Offers for promotion and ranking (real-time offers)”, which limits evaluating up to 50 offers for its promotion analysis and ranking.  
User attribute match criteria | 5 | —  
Segment inclusion | 10 | —  
Segment exclusion | 10 | —  
Attributes for a promotion | 35 | Promotion built-ins: 10, which means that you can add up to 25 user-created attributes.  
Related Catalog Objects | 20 | —  
Related Catalog Object values for a single item | 50 | —  
Assets for a promotion | 10 | —  
Assets assigned to a single content zone or tag | 1,000 | Applies across all promotions that share the content zone or tag.Example: If you have a content zone or tag called "Winter Savings," then you can have up to 1,000 assets across all your promotions that share the “Winter Savings” content zone or tag.If you have over 1,000 assets that share a content zone or tag, Personalization selects a random set of 1,000 for decisioning purposes.  
  
User Attribute Limits

Marketing Cloud Personalization has a limit of 100 user attributes per
dataset.

User Profile Object and Account Profile Attribute Limits

Marketing Cloud Personalization imposes limits per dataset for user profile
objects and account profile attributes. For more information, see [User
Profile
Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object.htm&language=en_US&type=5
"Gain a deeper understanding of your users by creating user profile
objects.").

Number of | Limit | Description  
---|---|---  
User profile object types | 10 | Examples: Lease, machine registration, mortgage  
Attributes for a user profile object | 10 | Example: If your user profile object is a mortgage, its attributes can include customer-specific information, such as start date, end date, and APR.  
Related catalog objects for a user profile object | 5 | Example: If your user profile object is a lease for a vehicle, you can assign it related catalog objects, such as make, model, and year.  
Values per related catalog object for a user profile object | 5 | Example: If your user profile object is a credit card and you assign it a related catalog object of rewards, associated values can include cash back, travel rewards, and no ATM fees.  
User profile objects per profile object type per user | 100 | Example: Suppose you’ve configured three profile objects: Lease, Ownership, and Service Case. Each user profile can have up to 100 objects of each type: up to 100 Lease objects, up to 100 Ownership objects, and up to 100 Service Case objects.  
Account profile attributes | 100 | Example: Account name, Account ID, Account domain, Employee count. Firmographic data that gives you a more in-depth profile of each account.  
Max distinct actions per profile per day  | 100 | Personalization tracks the number of distinct actions that a user takes on a website. For example, suppose a user visits the homepage 20 times, views the Product Detail Page 11 times, updates their billing information one time, and checks out twice. In this example, Personalization tracks four distinct actions for that user. The action limit applies to the number of distinct actions per user, not to the number of times a user performed a particular action. If the user exceeds the limit of distinct actions (say, 101 distinct actions over a 24-hour period), then Personalization truncates one of the distinct actions it’s tracking to keep the total within the limit. Personalization drops a distinct action with the lowest number of occurrences (for example, updating the billing information happened only one time). For an individual user, dropping a distinct action can affect segment membership.For more information on actions, see [Item Actions and Actions](https://developer.salesforce.com/docs/marketing/personalization/guide/item-actions.html) in the developer documentation.  
Max distinct actions per profile for All Time | 1,000 | Example: If a user exceeds 1000 distinct actions over time, then Personalization truncates one of the distinct actions it’s tracking to keep the total within the limit. For more information, see the example (in the previous row) for the maximum distinct actions per profile per day.  
Max number of line items in a cart | 100 | The total number of line items stored in a cart for a single user.  
  
Identity Management

Marketing Cloud Personalization imposes limits for identity types. For more
information, see [Identity Types and
Attributes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_type_attributes.htm&language=en_US&type=5
"Personalization’s identity system uses deterministic matching to create a
Unified Customer Profile for each of your customers. Specific identifiers,
called identity types, determine how to process web events, API events, and
channel events to identify users from various sources. Personalization
includes several built-in identity types, such as email address and customer
ID. If the built-in identity types don’t meet the needs of your organization,
you can create additional identity types.").

Number of | Limit | Description  
---|---|---  
Additional identity types | 3 | If the built-in identity types are insufficient, you can create a maximum of 3 additional identity types.  
  
## Integrations Limits

There are limits on ETL integrations, the integration of Personalization with
Salesforce CRM, and the automated data sent to Personalization using Flows.
For more information, see [Integrate with Other
Products](https://help.salesforce.com/s/articleView?id=sf.mc_pers_integration.htm&language=en_US&type=5
"Exchange data between Marketing Cloud Personalization and other systems,
including other Salesforce products.").

ETL Integrations

There are limits to some attributes and associations per item. Exceeding these
limits causes a record to fail.

Number of | Limit  
---|---  
Line items per order | 1000  
User attributes per user feed | 50  
Attributes per catalog object type | 35  
  
There’s no file size limit. However, Salesforce recommends limiting file sizes
to 5 GB.

Individual customer ingestion speeds can vary based on a number of factors,
including:

  * Number of users in the dataset
  * Time of day when an ETL job is started (other ETLs are running at the same time)
  * Number of user attributes in the feed and size of attribute values (for example, the length of strings)
  * Size of files being run (number of attributes in the file)
  * Size of user profile documents, which includes visit history, number of attributes, the change history of said attributes, visit history, and daily stats.

Customers can export up to 10 million users per day per dataset. For more
information, see [Personalization Editions—Growth and
Premium](https://help.salesforce.com/s/articleView?id=sf.mc_pers_editions.htm&language=en_US&type=5
"Marketing Cloud Personalization comes in two editions: Growth and Premium.").

Integrate Personalization with Salesforce CRM

For more information, see [Integrate Personalization with Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm.htm&language=en_US&type=5
"Share data between Marketing Cloud Personalization and Salesforce CRM. Send
Personalization user and visitor information to Salesforce CRM. Receive CRM
data associated with text fields, dropdown menus, numeric values, or
segments.").

Number of | Limit | Description  
---|---|---  
Salesforce CRM Pull limit of records | 4,500,000 | Limit per job or manual execution.  
Salesforce CRM Push limit of records  | 750,000 | Limit per job or manual execution.  
  
Automate Data Sent for Personalization Using Flows

For more information, see [Automate Data Sent for Personalization Using
Flows](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_sales_service_cloud_mgd_pkg_automate_data_w_flows.htm&language=en_US&type=5
"Automatically send data that is specific to a Named Individual Profile from
Sales or Service Cloud to Personalization.").

Number of | Limit  
---|---  
Maximum number of records that the Personalization Apex Action can process | 100  
  
![3f96c663-7a12-4471-8ca7-54037ccb1368]

Note Apex Execution Governors and Limits restricts the total number of
callouts (HTTP requests or web services calls) in a transaction to 100. You
can increase the batch size from the default of 25 to 100 with the removal of
runtime validation for datasets, attributes, and profile objects. For more
information, see [Execution Governors and
Limits](https://developer.salesforce.com/docs/atlas.en-
us.250.0.apexcode.meta/apexcode/apex_gov_limits.htm).

## Segment Management Limits

Marketing Cloud Personalization provides the following limit associated with
segment membership. For more information, see
[Segments](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment.htm&language=en_US&type=5
"Audiences are the specific individuals, referred to as users, or accounts,
such as companies and organizations, that qualify to be members of a segment.
You can create segments to group audiences according to a set of criteria that
you define.").

Number of | Limit  
---|---  
Manual segments per dataset | 1,000  
Enabled rule-based segments per dataset | 500  
  
## Channels and Campaigns Limits

Marketing Cloud Personalization provides limits specific to Web Campaigns,
Mobile Campaigns, and Triggered Campaigns. For more information, see [Channels
and
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_channel_campaign.htm&language=en_US&type=5
"In Personalization, channels are the various digital touch points you use to
interact and engage with your customers and leads. Campaigns are the heart of
providing personalized experiences within each of those channels. Depending on
your Marketing Cloud Personalization license, you have access to develop
campaigns for channels such as web, email, mobile, and third-party
integrations.").

Web Campaigns

The Web SDK automatically blocks events if:

  * more than 10 events have been sent for the same user in the last 5 seconds, or
  * more than 5 events with the same interaction name (Action) have been sent for the user in the last 2 seconds.

In addition to the above limits, the Web SDK enforces the following limits for
ping, error, and campaign statistics events.

  * Ping events are limited to 10 events sent every 5 seconds.
  * Error events are limited to 10 events sent every 5 seconds.
  * Campaign statistics events are limited to 10 events sent every 5 seconds, or 5 events with the same experience ID sent every 2 seconds.

Mobile Campaigns

The Personalization Mobile SDK supports up to 50 events per second. Up to
1,000 events can be queued when:

  * the device isn’t connected to the internet, or 
  * the Mobile SDK is waiting for the response of the previously sent event.

Triggered Campaigns

Salesforce limits the number of triggers based on your contracted number of
named individual profiles. Each named individual profile is entitled to four
triggers per month, with the trigger limit calculated for an hourly rate. For
example, using the base allotment of 100,000 named individual profiles, the
per profile rate is approximately 555 triggers per hour:

    
    
    (Named individual profiles x 4) / 30 days / 24 hours = 555 triggers/hour

![8bc2a0eb-623c-4caa-9d0a-c3bd39139cbd]

Important Exceeding this rate results in messages being delayed. Continuing to
exceed this rate for multiple hours can result in messages being dropped.

Survey Limits

Marketing Cloud Personalization has limits for survey attributes. You can have
up to 10 total survey attributes per dataset. For more information, see [Use
Surveys in Web
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_survey.htm&language=en_US&type=5
"Use surveys to design, test, and deploy questions to your visitors and
customers to gather feedback in web campaigns.").

Open-Time Email Campaign Limits

For more information, see [Open Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign.htm&language=en_US&type=5
"Use open time email campaigns to deliver personalized content and product
recommendations each time a recipient opens an email. Using existing email
campaigns that you send using your mail marketing service, Open Time Email
campaigns deliver real-time personalized content to each member of your
subscriber list.").

Number of | Limit | Description  
---|---|---  
Item Templates that can be published | 16 | —  
Item Template sync error rate per job | 10% | If the error rate for an image generation job exceeds 10%, the item template can’t be published.  
  
Third-party Campaigns

You can have a maximum of 900 third-party campaigns. For more information, see
[About Integrating with Third-Party
Solutions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_third_party_integration_about.htm&language=en_US&type=5
"Marketing Cloud Personalization integrates with a variety of third-party
solutions \(external to Salesforce\). Integration options include data
management platforms, email service providers, third-party campaign detection
products, analytics products, content management systems, social media, and
tag managers.").

## Machine Learning Limits

Marketing Cloud Personalization provides limits associated with Einstein
Decisions and Einstein Recipes. For more information, see [AI-Powered
Personalization](https://help.salesforce.com/s/articleView?id=sf.mc_pers_machine_learning.htm&language=en_US&type=5
"Marketing Cloud Personalization uses advanced machine learning algorithms to
capture a deep understanding of your business and your users. Einstein Recipes
and Einstein Decisions use those algorithms to present personalized
recommendations and offer the most relevant experiences to your users in real
time.").

Einstein Decisions Limits

Marketing Cloud Personalization has limits for the various Einstein Decisions
features. For more information, see [Einstein
Decisions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_decision.htm&language=en_US&type=5
"When a user views a promotion on your website, Marketing Cloud
Personalization captures the user's context—including whether they’re a
returning visitor, the device they’re using, and other information that
provides insight into that user. Einstein Decisions, Personalization’s machine
learning approach for next-best-offer decisioning, uses that context to
predict the value of showing a specific offer to a particular user.").

Number of | Limit | Description  
---|---|---  
Features | 200 | You can configure up to 200 features on the feature engineering page.  
Offers for promotion and ranking (real-time offers) | 50 | Personalization limits Einstein Decisions to evaluating up to 50 offers for its promotion analysis and ranking. If a user is eligible for more than 50 offers, Personalization selects a randomized set of the eligible offers for analysis.  
Promotions in a Campaign Response | 12 | A campaign using Einstein Decisions can return up to 12 promotions in a response.  
  
Einstein Recipes Limits

Marketing Cloud Personalization has limits for the various Einstein Recipes
features. For more information, see [Einstein
Recipes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_recipe.htm&language=en_US&type=5
"Einstein Recipes are Personalization's machine learning algorithms. With
Einstein Recipes, you can create configurable algorithmic strategies to
present each customer with customized product and content recommendations
throughout your various channels. You can use Einstein Recipes to support
specific scenarios, such as cross-sells, content promotions, and trending
products.").

  * Test groups can contain a maximum of 20 customers.
  * You can have up to 15 test groups, including the sample test group.

## Reports and Analytics Limits

Marketing Cloud Personalization provides limits associated with Actions
Reports and Data Warehouse. For more information, see [Reports and
Analytics](https://help.salesforce.com/s/articleView?id=sf.mc_pers_report_analytics.htm&language=en_US&type=5
"After personalizing your site, use Personalization reports to determine
what’s working and where to make improvements.").

Actions Report

Marketing Cloud Personalization supports a few thousand unique actions. Unique
action counts that are larger than a few thousand can cause problems in
various areas of the platform.

Actions should be captured only if they’re required for personalization and
targeting. Marketing Cloud Personalization isn’t designed to act as an
analytical store, and thus shouldn’t have an implementation where actions are
blindly consumed from an analytics provider like Google Analytics. The sitemap
is meant to provide customers with a transform layer to ensure that only the
necessary data is ingested.

Data Warehouse Limits

![95b39cf2-c74e-4e1c-9361-a100f2c79b7c]

Note [](https://help.salesforce.com/s?language=en_US)The Data Warehouse is
available only for customers who have already purchased the Marketing Cloud
Personalization \- Data Warehouse add-on product.

The Marketing Cloud Personalization Data Warehouse environment allows for:

Number of | Limit  
---|---  
Named users | 6  
Datasets | 6  
Segments | 10  
  
Data Warehouse targets a 24-hour window from the time of initial receipt to
make the data available. Nightly jobs often complete by 6pm UTC. Data
Warehouse job processing and completion times can vary.

For more information, see [Personalization Data
Warehouse](https://help.salesforce.com/s/articleView?id=sf.mc_pers_data_warehouse.htm&language=en_US&type=5
"Marketing Cloud Personalization tracks and measures engagement—at the
individual and account levels—across your company’s channels. The Data
Warehouse is a repository of personalization data that is optimized for
analysis. Business analysts can use their preferred business intelligence
\(BI\) tool to access the Data Warehouse and run queries to transform, report
on, analyze, and visualize your Marketing Cloud Personalization data.").

#### See Also

  * [Personalization Editions—Growth and Premium](https://help.salesforce.com/s/articleView?id=sf.mc_pers_editions.htm&language=en_US&type=5 "Marketing Cloud Personalization comes in two editions: Growth and Premium.")

