

# Strict Catalog Security

When adding or updating catalog objects, use the Strict Catalog Security
setting to determine how Personalization adds new items to your catalog, and
how it updates an item’s information. When you enable the Strict Catalog
Security setting, Personalization ignores catalog item metadata, such as
attributes, unless it comes from a feed or an authenticated event source.

When you enable Strict Catalog Security for a dataset, Personalization only
updates item attributes for an authenticated source. For events from an
unauthenticated source, Personalization performs the following actions:

  * Tracking of statistics, such as clicks, views, purchases, and favorites, for the item ID and associated item metadata, such as related catalog objects

  * Creating new, top-level-only catalog items and applying related catalog object information for an item 

To update attribute metadata about a catalog object with this setting enabled,
you must use a trusted method, such as ETL or an authenticated event API.

Access the Strict Catalog Security setting from the main navigation by selecting **Settings** | **Catalog and Profile Objects**.

When you disable Strict Catalog Security for a dataset, any
event—authenticated or unauthenticated—can update catalog items and their
associated data, in addition to statistics tracking. This approach can provide
better support for real-time catalog updates. Example use cases include:

Item | Description  
---|---  
Updates to existing item attributes and related catalog objects | If someone browses a product on your site that has a recent price change, Personalization can update its catalog price in real time. With Strict Catalog Security enabled, an attribute update, such as a price change, must come from an authenticated source.  
New item addition | If a customer browses an item that you just added, Personalization creates a full listing for it and that item can be a recommendation for an Einstein Recipe. With Strict Catalog Security enabled, Personalization creates a top-level listing with related catalog object metadata, but doesn’t populate attribute data, even if it’s included in the event. The item isn’t promotable in Einstein Recipes until an authenticated source (ETL or API) updates the parameters necessary to include it in a recommendation.

