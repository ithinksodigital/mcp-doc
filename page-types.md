# Page Types

Page Types are used to establish what pages on a website and what data on
these pages you'd like Marketing Cloud Personalization to track. Page Types
also define the Content Zones, Events, Templates, and Catalog data to be
tracked by Personalization on a page. An Personalization Sitemap comprises
multiple `pageType` configurations. You can apply a single `pageType`
configuration to multiple pages on your website.

The following table summarizes the fields that a `PageConfig` accepts.

Field Name| Expected Value Type| Required| Description| Namespace  
---|---|---|---|---  
`name`| String| **Yes**|  The name of the page type. Example: Homepage,
Product Detail| Both  
`isMatch`| `() => boolean | () => Promise<boolean>`| **Yes**|  The function that determines if the current page matches the config| Both  
`action`| String| No| The action that is sent when the config is evaluated|
`Evergage`  
`itemAction`| String| No| The property of ActionEvent used to identify user
actions taken on catalog items such as "Purchase" or "AddToCart".| `Evergage`  
`interaction`| `Interaction`| No| The property of `ActionEvent` used to
identify user actions taken on catalog items such as "Purchase" or
"AddToCart".| `SalesforceInteractions`  
`catalog`| `CatalogConfig`| No| The catalog data to be captured| `Evergage`  
`cart`| `CartConfig`| No| The cart data to be captured| `Evergage`  
`order`| `OrderConfig`| No| The order data to be captured| `Evergage`  
`contentZones`| `ContentZone[]`| No| The content zones defined on the page|
Both  
`listeners`| `Listener[]`| No| The event listeners to be bound when this
configuration is evaluated| Both  
`onActionEvent`| `(event: ActionEvent) => ActionEvent`| No| The function to
modify the outgoing `ActionEvent`| Both  
  
Depending on your business vertical, the objective of your website, and the
type of content it serves, certain page types are recommended to be mapped
over others.

The following table outlines general page types that you can define on any
website.

Page Type| Description  
---|---  
`home`| The website's homepage  
`blog`| The blog's homepage  
`blog_detail`| A blog post  
`search`| The search page  
`search_results`| The search results page  
`register`| The register page  
`sign_in`| The sign-in page  
`account`| The account overview page  
`error_page`| An error page. Example: 404 Page  
  
The following table outlines page types that are recommended for a commerce
website.

Page Type| Description  
---|---  
`product_detail`| A product detail page  
`brand`| A brand detail page  
`department`| A department overview page  
`category`| A category page, sometimes referred to as a product list page  
`cart`| The shopping cart  
`checkout`| The checkout pages  
`order_confirmation`| The order confirmation page  
  
The following table outlines page types that are recommended for a B2B
website.

Page Type| Description  
---|---  
`product`| A specific product offering  
`solution`| A group of offerings, high-level capability, or industry  
`article`| A details page for articles. For example, White Papers, Technical
Specs  
`event`| A details page for events. For example, Webinars, Conferences  
`learning`| A details page for learning content. For example, Classes,
Playbooks, Forums, Documentation  
  
The following table outlines the naming convention to follow for the
`pageTypeDefault` configuration in the sitemap.

Page Type| Description  
---|---  
`default`| Any page that isn't explicitly mapped

