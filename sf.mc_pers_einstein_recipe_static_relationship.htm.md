

# Use a Static Relationship in an Einstein Recipe

After you associate products with each other in a static relationship, you can
use it as an ingredient in Einstein Recipes to define which products to
recommend with other products. When making recommendations, Personalization
considers any static relationships you’ve configured.

### Required User Permissions

Permissions Needed  
---  
To add static relationships: | A role with Recipes Create/Edit permissions  
  
![edc3a6e8-8942-49be-9c89-128d742fd01e]

Note This ingredient is available only if:

  * You have Static Relationships enabled for your account, and
  * You’re tracking products on the dataset.

  1. Before you can use the static relationship ingredient in an Einstein Recipe, you must define static relationships to associate products with one another in your catalog. For more information, see [Define Static Relationships](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_static_relationship_define.htm&language=en_US&type=5 "Define static relationships to associate products with one another in your catalog. You can use static relationships as ingredients in Einstein Recipes to help determine which additional related products to recommend to your customers.").
  2. In the **Machine Learning** section of the main navigation, click **Einstein Recipes.**
  3. Click **New Recipe**.
  4. Enter a **Name** for the recipe.
  5. Click **Recommendation Type** and select **Product** from the dropdown.
  6. On the **Ingredients** tab, click **Add ingredient** and select **Static Relationship** from the dropdown.
  7. Select parameters for the ingredient.
  8. Add additional ingredients, exclusions, inclusions, boosters, and variations as necessary.
  9. Save your work.

