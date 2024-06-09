

# Assign Static Relationships Manually

After you define static relationships for your catalog, you can associate
products with one another. You can then use static relationships in an
Einstein Recipe so that Personalization can recommend associated products to
your customers. Before you can associate products with one another in a static
relationship, you must define the static relationships for your catalog.

### Required User Permissions

Permissions Needed  
---  
To assign static relationships: | A role with Catalog Create/Edit permissions  
  
![248e5260-c1ab-45d7-8c5d-4dcc4fa0e62c]

Note If you have a large number of products to associate in a static
relationship, you can upload a CSV file rather than follow this manual
process. For more information, see [Upload Static
Relationships](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_static_relationship_upload.htm&language=en_US&type=5
"After you define static relationships for your catalog, you can upload a CSV
file to associate products with each other. You can then use static
relationships in an Einstein Recipe so that Personalization can recommend
associated products to your customers.").

  1. In the **Catalog** section of the main navigation, select **Catalog** | **Products**.
  2. Select the product you want to associate another product with, and click **Edit**.

![2f18d597-2275-4013-bc67-d1a4e616be22]

Note The product you select is called the anchor product.

  3. Click the **Relationships** tab.
  4. Click **Add Product** for the static relationship you want to use.
  5. To search for the product you want to associate with the anchor product, enter the product name or ID.
  6. Select the product from the list of options.
  7. Add any additional products you want to associate with the anchor product, using the same static relationship or a different one.

![c0d1ef91-d504-466a-bffa-961d1f7b01ff]

Note The product association isn’t bidirectional. For example, if product A is
the anchor product and you associate product B with it, only product B returns
for product A. For product A to also return for product B, you must also
associate product A with product B when product B is the anchor product.

  8. When you finish, click the **Details** tab.
  9. Click **Save**.

![7e9b3e46-0215-4255-8e3d-ec0ecc8c6549]

Note When you use the static relationships in an Einstein Recipe,
Personalization recommends all associated products for that anchor product.

#### See Also

  * [Upload Static Relationships](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_static_relationship_upload.htm&language=en_US&type=5 "After you define static relationships for your catalog, you can upload a CSV file to associate products with each other. You can then use static relationships in an Einstein Recipe so that Personalization can recommend associated products to your customers.")
  * [Use a SmartBundle Relationship in an Einstein Recipe](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_recipe_smartbundle_relationship.htm&language=en_US&type=5 "After you associate categories with each other in a SmartBundle relationship, you can use the SmartBundle ingredient in Einstein Recipes to define which items to recommend with other items. When making recommendations, Personalization considers items from SmartBundle-related categories that customers bought together in the same cart.")

