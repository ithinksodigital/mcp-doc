

# Use a Static List in an Einstein Recipe

Use static lists that you create in Einstein Recipes as exclusions,
inclusions, or boosters.

### Required User Permissions

Permissions Needed  
---  
To create a recipe: | A role with Create/Edit permissions  
  
  1. Create a static list of products in a CSV file and upload it so you can use it in an Einstein Recipe. For more information, see [Create a Static List](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_static_list_create.htm&language=en_US&type=5 "Use the StaticList tag to group products together in a static list. You can upload a comma-separated values \(CSV\) file of products to a static list, and then use that list in Einstein Recipes as an exclusion, inclusion, or booster."). 
  2. In the **Machine Learning** section of the navigation pane, select **Einstein Recipes**.
  3. Click **New Recipe**.
  4. Enter a **Name**.
  5. Click **Add Ingredient** and select an ingredient.
  6. To add a static list as an exclusion, click **Exclusions** , click **Add exclusion** , and select **Product List** from the list.
  7. To add a static list as an inclusion, click **Exclusions** , click **Add exclusion** , select **Product List** from the list, and then click **Include**.
  8. To add a static list as a booster, click **Boosters** , click **Add Booster** , and select **Product List** from the list.

![5756d798-ccc9-4416-8fc4-788ade177151]

Note You can only use a static list as a booster when recommending a product,
article, or blog post.

  9. Click **Save**.

