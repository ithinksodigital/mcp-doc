

# Create a Static List

Use the StaticList tag to group products together in a static list. You can
upload a comma-separated values (CSV) file of products to a static list, and
then use that list in Einstein Recipes as an exclusion, inclusion, or booster.

### Required User Permissions

Permissions Needed  
---  
To create a static list: | A role with Catalog Create/Edit permissions  
  
  1. Create a CSV file by entering “products” into cell A1 and, starting at cell A2, the product IDs for each product to associate (or disassociate) with the StaticList tag.
  2. From the main navigation, select **Settings** | **Catalog and Profile Objects**.
  3. Click the **+** beside **Catalog Object Types**.
  4. Enter “StaticList” as the **Name** and “Product List” as the **Label**.
  5. Turn on the **Enabled** option.
  6. Click **Save**.
  7. Refresh your browser.
  8. In the **Catalog** section of the main navigation, select **Catalog** | **Product Lists**.
  9. Click **Upload Product List** in the upper right corner.
  10. In the **Upload New Product List** dialog, enter a tag ID.
  11. If you’re removing the tag from the list of products, select **Remove tag from items**.
  12. Click **Upload Product List**.
  13. Click **Select files** to locate and select your CVS file, or drag the file within the dotted lines of the dialog.

![995f2ab1-f8dd-4001-8ffc-2e0bd3db2a56]

Example

![8897bcf0-a9fb-42f9-9a7d-a90518e97c4f]

#### See Also

  * [Catalog Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object.htm&language=en_US&type=5 "Catalog objects and their relationships define the structure of your catalog. Personalization uses catalog objects to interpret and understand customer engagement and affinities. Examples of catalog objects include products, articles, blog posts, categories, brands, styles, and features. Personalization includes several built-in catalog objects, and you can create custom ones to meet your specific needs.")
  * [Einstein Recipes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_recipe.htm&language=en_US&type=5 "Einstein Recipes are Personalization's machine learning algorithms. With Einstein Recipes, you can create configurable algorithmic strategies to present each customer with customized product and content recommendations throughout your various channels. You can use Einstein Recipes to support specific scenarios, such as cross-sells, content promotions, and trending products.")

