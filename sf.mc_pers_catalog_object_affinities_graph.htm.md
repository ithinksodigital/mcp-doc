

# Customizing the Affinities Graph

The Affinities graph displays affinities for objects that use a specific
catalog object type as their Name value. You can define custom catalog objects
to appear in the Affinities graph when viewing a unified customer profile.

The default object types are Category, Style, Brand, and ItemClass. The
Category object type is static and can’t be changed. However, you can use the
Style, Brand, or ItemClass object type to display affinities for a catalog
object that has one of these values in its **Name** field, even if the catalog
object doesn’t match the object type. For the objects using these values, the
Affinities graph uses the value in the object’s **Label** field to populate
the display name in the graph.

As an example, for an apparel-related ecommerce site, you can configure the
Affinities graph to show affinities for COLOR (Style), BRAND (Brand), or
PRODUCT CLASS (ItemClass).

![5395827a-0cc2-43af-8b6f-7319c6885c28]

For a site selling books, you can replace the apparel-related labels to show
affinities for different catalog objects, like GENRE (Style), AUTHOR (Brand),
and AGE GROUP (ItemClass).

![46fac2f8-5ad4-441f-866c-7c487d83d5f1]

When customizing the Affinities graph, keep these considerations in mind.

  * When defining a custom catalog object, you can use either an existing custom catalog object or create a new custom catalog object.
  * You can’t change a Name value after you save a catalog object. For this reason, if you choose to modify an existing custom catalog object you can modify only the **Label** value to change the Affinity display. If you choose to create a new custom catalog object, you must delete the existing catalog object that uses the Affinity graph **Name** value you plan to use for the new object.

#### See Also

  * [Create a Custom Catalog Object](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_custom.htm&language=en_US&type=5 "Personalization collects behavioral data in the context of the catalog that you create and uses catalog objects to assess and analyze customer engagement and affinities. You can add more detail to your catalog by using custom objects. The more detailed you make your catalog, the more granular your insights are regarding customer engagement and affinity.")
  * [Unified Customer Profile for Demand Generation](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_customer_profile_for_demand_generation.htm&language=en_US&type=5 "The Unified Customer Profile provides an overview of the information that Personalization collects about a particular user. The information that is shown depends on the type of business you select \(demand generation\).")
  * [Unified Customer Profile for Ecommerce](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_customer_profile_for_ecommerce.htm&language=en_US&type=5 "The Unified Customer Profile provides an overview of the information that Personalization collects about a particular user. The information that is shown depends on the type of business you select \(ecommerce\).")

