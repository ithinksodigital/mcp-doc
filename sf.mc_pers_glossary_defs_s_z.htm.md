

# S - Z

Marketing Cloud Personalization common terms from S to Z.

![90274c33-8859-4f4d-9bbe-ac3c6a119d22]

Note This glossary contains many, but not all, common terms associated with
Marketing Cloud Personalization. If you don't see a term defined here, search
for it using the search box in the left panel.

  * **[Salesforce Interactions SDK Launcher](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_interactions_sdk_launcher)**  

  * **[segment](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_segment)**  

  * **[server-side campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_server_side_campaign)**  

  * **[similar items ingredient](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_similar_items_ingredient)**  

  * **[sitemap](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_sitemap)**  

  * **[smartBundle ingredient](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_smartbundle_ingredient)**  

  * **[soon to expire ingredient](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_soon_to_expire_ingredient)**  

  * **[statistical significance](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_statistical_significance)**  

  * **[target page](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_target_page)**  

  * **[Technology report](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_technology_report)**  

  * **[threshold](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_threshold)**  

  * **[traffic source](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_traffic_source)**  

  * **[train](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_train)**  

  * **[trending ingredient](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_trending_ingredient)**  

  * **[unified customer profile](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_unified_customer_profile)**  

  * **[unique visitor](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_unique_visitor)**  

  * **[user](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_user)**  

  * **[visit](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_visit)**  

  * **[visitor](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_visitor)**  

  * **[visits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_visits)**  

  * **[weight](https://help.salesforce.com/s/articleView?id=sf.mc_pers_glossary_defs_s_z.htm&language=en_US&type=5#mc_pers_glossary_weight)**  

[](https://help.salesforce.com/s?language=en_US)

## Salesforce Interactions SDK Launcher

A Google Chrome browser extension used to add personalization features to a
website. With developer-created templates, you can create personalization
campaigns targeted to specific groups, individual users, or events.

[](https://help.salesforce.com/s?language=en_US)

## segment

Real-time grouping of accounts or individuals based on a defined set of criteria. Segments are used in many ways, including analytics, campaign goals, and even to set parameters for rule-based campaigns. Segment updates happen in real time, so any membership changes occur immediately, even during the same visit. Segments can be user-based or account-based.  Segment Type | Description  
---|---  
user segments | Represent individuals who visit the site or log into the application.  
account segments | Require B2B detect on a site. They’re segments of companies and are typically used to target visitors coming from a particular organization.  
Use segments declared as filters to filter reports. Apply segments declared as
goals to campaigns for measuring lift. For the sake of reporting, goal
segments are also considered filter segments.

[](https://help.salesforce.com/s?language=en_US)

## server-side campaign

A campaign that integrates Marketing Cloud Personalization testing and
personalization at the server-to-server level.

For these campaigns, your server calls the Marketing Cloud Personalization
server-side campaign API and provides information about the visitor (typically
the user ID). Based on that information, Marketing Cloud Personalization
handles the campaign logic and returns recommendations and other campaign data
(in JSON format) that applies to that visitor. Your server is responsible for:

  * handling the JSON
  * building the message to show the visitor
  * calling the appropriate action-tracking APIs to track campaign impressions and clicks

While Marketing Cloud Personalization handles the campaign logic, a developer
is required to write the code to:

  * call the appropriate APIs
  * provide Marketing Cloud Personalization with the necessary information about the visitor viewing the campaign

[](https://help.salesforce.com/s?language=en_US)

## similar items ingredient

An algorithm that returns recommendation results for products or content that
are similar in nature to:

  * the item that a visitor is viewing, or
  * the item that a visitor has placed in the cart

The Similar Items ingredient is often used on a product display page to help
visitors discover more products. It typically appears at the bottom of the
page with a label like "Other Similar Products".

[](https://help.salesforce.com/s?language=en_US)

## sitemap

Marketing Cloud Personalization’s sitemap framework is a configuration-driven
integration layer that is deployed by, and executes within, the Marketing
Cloud Personalization beacon. A sitemap is developed to integrate with a
specific site using APIs that map key business objects into Marketing Cloud
Personalization through event capture. To help understand user interests
against the catalog, the sitemap can include page type information and catalog
items. It can also include:

  * items such as products, article content, and categories
  * custom dimensions, which are categorical information about items with custom attributes

Situational data includes such information as a visitor's referring site,
email or ad campaign source, IP address, geo-location, device type, and
operating system.

[](https://help.salesforce.com/s?language=en_US)

## smartBundle ingredient

A merchandising algorithm that analyzes products that are bought together in
the same cart and returns recommendations based on explicitly defined
categories. With this ingredient, Marketing Cloud Personalization recommends
paired items that are commonly bought together. For example, if the visitor is
viewing men’s dress shirts, this ingredient can show items in the “tie”
category.

[](https://help.salesforce.com/s?language=en_US)

## soon to expire ingredient

An algorithm that uses the expiration date captured in the catalog. Use this
ingredient to prioritize items that are about to expire.

[](https://help.salesforce.com/s?language=en_US)

## statistical significance

A measure of how certain you can be with the reported lift. A metric is
determined to be statistically significant based on a number of factors built
into Marketing Cloud Personalization algorithms.

[](https://help.salesforce.com/s?language=en_US)

## target page

Add to a rule to specify where to display the campaign or message. For
example, you can set a rule so that the campaign appears only on the desired
pages and nowhere else.

[](https://help.salesforce.com/s?language=en_US)

## Technology report

Provides insight into the types of browsers and devices that visitors are
using when they view the site. Informs you about how visitors are interacting
with the site so that you can set up campaigns accordingly. For example,
knowing whether visitors are accessing your site from a mobile device helps
you determine whether to develop campaigns for mobile browsers.

[](https://help.salesforce.com/s?language=en_US)

## threshold

Determines the point at which a visitor is considered affine for the booster.
The slider has five positions with the first position being the lowest
weighting and fifth, the highest. Move the slider to specify how much a
visitor must interact with the selected affinity to be considered affine and
boost products from that affinity. After the visitor meets that threshold,
Marketing Cloud Personalization boosts products within that affinity.

[](https://help.salesforce.com/s?language=en_US)

## traffic source

Indicates where a visitor originated from before they came to your site.
Examples include social media, search based on search terms entered, and other
types of websites.

[](https://help.salesforce.com/s?language=en_US)

## train

A process in which a recipe:

  * reviews all of the implicit and explicit data that Marketing Cloud Personalization continuously collects about each visitor
  * learns about the different data points, and
  * compiles the ingredients (algorithms) that powers the recommendation.

[](https://help.salesforce.com/s?language=en_US)

## trending ingredient

An algorithm that recommends products or content based on what’s trending on
the site right now. Define this ingredient to display items or content based
on the highest number of purchases or downloads, the most revenue generated,
the most views, or the most time spent viewing.

[](https://help.salesforce.com/s?language=en_US)

## unified customer profile

A visual representation of all the data about a single visitor, including
preferences and affinities. Roll this profile up to the account level to view
the relationships among visitor behaviors associated with the same account.

[](https://help.salesforce.com/s?language=en_US)

## unique visitor

The total number of tracked individuals who have seen a campaign.

[](https://help.salesforce.com/s?language=en_US)

## user

A visitor to a client website.

[](https://help.salesforce.com/s?language=en_US)

## visit

Starts from the first page view and ends after the user reaches 30 minutes of
inactivity on the site. For example, suppose a user visits the homepage for
the first time, leaves, and then returns to the site 29 minutes later. The
page views are still considered to be part of the first visit. It’s important
to remember how visits are calculated when testing campaign targeting rules
based on visit count.

[](https://help.salesforce.com/s?language=en_US)

## visitor

Represents an individual user or visitor to your site. In reports, the
visitors statistic shows the number of unique daily visitors and the number of
visits during the selected timeframe. An indicator shows whether traffic is up
or down, where visitors are coming from, and whether they’re known or
anonymous users.

[](https://help.salesforce.com/s?language=en_US)

## visits

Counts all visitors’ sessions on the site, regardless of how many times the
same visitor has been to the site.

[](https://help.salesforce.com/s?language=en_US)

## weight

An ingredient setting that determines the order in which an item is displayed
in a recipe. Every item returned by an ingredient has a weight. Items with the
highest weight are displayed first by the recipe. To control how an ingredient
is weighted against other ingredients in the same recipe, increase or decrease
the weight and importance of items returned by the ingredient. Marketing Cloud
Personalization then multiplies the scores for the items returned for the
ingredient by the assigned weight, and displays the top weighted items.
Because the recipe attempts to return items for the ingredient with the
highest weight first, assign the highest weight to your highest priority
ingredient.

