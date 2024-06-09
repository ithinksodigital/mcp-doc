

# Built-In Catalog Objects

Built-in catalog objects enable you to quickly begin building your catalog and
define its structure. Personalization uses catalog objects to interpret and
understand customer engagement and affinities. Personalization collects
behavioral data about your customers in the context of your catalog. Catalog
objects can be standalone entities, or they can relate to one another to
provide a more granular structure for your catalog.

Built-in catalog objects include these items.

Item | Description  
---|---  
Product | Product is the only catalog object that has pricing, inventory, and SKU support. Products are also the only catalog object that a customer can purchase or add to a cart. Products can’t be a related catalog object for another catalog object.  
Article and blog post | Articles and blog posts don’t have any special or unique characteristics. However, they can’t be a related catalog object for another catalog object.  
Category | Category is a related catalog object for product, blog post, and article catalog objects. The cardinality value you select for category (One per Item or Many per Item) applies to all its associated catalog objects. Category can’t be a related catalog object for custom catalog objects.  
  
Products, blog posts, and articles also have an optional base URL setting that
you can use if your catalog items have relative URLs.

## Related Catalog Objects

You can relate catalog objects to one another to provide a more granular
structure for your catalog. For example, adding brands as a related catalog
object for products helps you create logical subdivisions. Adding other
related catalog objects, such as features, sizes, and colors, provides more
granularity for your products.

You can also add related catalog objects to promotions to improve Einstein
Decisions for personalized next best offer recommendations. Related catalog
objects help define affinity and interaction data across your entire business.

## Cardinality for Related Catalog Objects

When you relate catalog objects to one another, you define the cardinality of
that relationship using one of these options.

  * One per SKU:

![b62a00d9-aaa5-4fd8-8dac-f5287cbb317f]

Note This option applies only to the built-in Product catalog object.

    * If the `relatedCatalogObject` type is present in an item action event—Personalization adds it to the item's set of catalog objects and tracks statistics for that catalog object only.
    * If the `relatedCatalogObject` type isn’t present in an item action event—Personalization doesn’t track statistics for any existing catalog objects, unless there’s exactly one of that existing catalog object.
  * One per item:

    * If the `relatedCatalogObject` type is present in an item action event—Personalization sets the catalog objects for that type on the item, replacing any existing catalog objects for that type. If there’s more than one in the event, Personalization uses only the first in the list. Personalization also tracks statistics for the catalog object.
    * If the `relatedCatalogObject` type isn’t present in an item action event—Personalization tracks statistics for an existing catalog object of that type if one exists for the item.
  * Many per item:

    * If the `relatedCatalogObject` type is present in an item action event—Personalization adds it to the item's set of catalog objects. Personalization also tracks statistics for all of the catalog objects for that type associated with the item.

    * If the `relatedCatalogObject` type isn’t present in an item action event—Personalization tracks statistics for all existing catalog objects of that type associated with the item.

## Catalog Object Attributes

Catalog object attributes provide metadata that Personalization uses when
managing data. Examples of attributes include ID, name, URL, dates, inventory,
price, currency, and rating.

## Stock Keeping Units

Stock Keeping Units (SKUs) are optional metadata of the Product built-in
catalog object. They're unique identifiers that you can assign to variants of
products in your catalog. You can assign child SKU IDs to a parent Product ID
to represent variations of the same product, such as distinct patterns of a
shirt. The SKUs you assign to a product appear on the product's Item Edit
screen and its statistics report on the Personalization UI.

You can use SKUs to organize and differentiate products in your catalog if
your website features product families and a single Product Detail Page (PDP)
displays variants of the same product. For example, you can use a unique child
SKU ID to represent each distinct pattern of a shirt in your catalog, all
connected to a single parent Product ID.

You can also use SKUs for purchase tracking if your website's purchase flow
excludes Product IDs and includes only an SKU ID on the purchase confirmation
page. In such cases, if you have correctly associated Products with SKUs in
your catalog, Personalization uses SKU merging to track purchases back to
their associated Product IDs.

Since SKUs only work with the Product built-in catalog object, you can't use
them with any other built-in or custom catalog object type. You also can't use
SKUs with product recommendation campaigns. While SKUs are helpful in managing
your product catalog, not all integrations require the use of SKUs. We
recommend using them only if they meet your catalog management needs.

![e349f960-c5e6-431d-92a3-c4abc9bea9e6]

Note SKUs aren’t stored as an attribute or related catalog object of the
parent Product ID. Additionally, Product IDs and SKU IDs share a namespace.
Therefore, you must avoid using identical values for a Product ID and an SKU
ID in the same catalog. For example, avoid having both a Product ID and an SKU
ID set as `id001` in the same catalog.

#### See Also

  * [Create a Custom Catalog Object](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_custom.htm&language=en_US&type=5 "Personalization collects behavioral data in the context of the catalog that you create and uses catalog objects to assess and analyze customer engagement and affinities. You can add more detail to your catalog by using custom objects. The more detailed you make your catalog, the more granular your insights are regarding customer engagement and affinity.")
  * [Static Relationships](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_profile_static_relationship.htm&language=en_US&type=5 "Use static relationships as ingredients in Einstein Recipes to help determine which additional related products to recommend to your customers.")
  * [User Profile Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object.htm&language=en_US&type=5 "Gain a deeper understanding of your users by creating user profile objects.")

