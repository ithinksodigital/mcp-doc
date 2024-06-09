

# Exclusions and Inclusions in Einstein Recipes

Use exclusions and inclusions to add filtering criteria to your Einstein
Recipes to control which items to recommend to your customers. For example,
you can add an exclusion to show only items from the same category as the item
a customer is viewing. A customer who views a specific hat brand only sees
recommendations for other hats, and not items from the same brand.

When configuring exclusions or inclusions for Einstein recipes, keep the
following in mind:

  * Creating an exclusion for any items (articles, blogs, products, and so on) includes all other items that are not explicitly excluded.
  * Creating an inclusion for any items (articles, blogs, products, and so on) excludes all other items that are not explicitly included.
  * All applied exclusions and inclusions are evaluated using logical AND operations.
  * If a customer comments on an article or blog post, Personalization can save the article’s ID as a custom attribute called Most recently commented. If you exclude all articles or blogs with that custom attribute, Personalization doesn’t recommend the article or blog the customer most recently commented on.
  * Numerical attributes (**Integer** and **Decimal**) are not available selections when using the **From user attribute** option.
  * You define catalog objects as compatible or incompatible with one another through each item’s Relationship page in your catalog. This relationship association is unidirectional, so make sure to configure each related item.
  * Exclusion or Inclusion based on compatibility filters tags or categories using their compatibility with anchor items. For example, if you mark Brand A as incompatible with Brand B, and Brand A is an anchor item, Personalization doesn’t recommend anything from Brand B. Conversely, if you mark Brand A as compatible with Brand B, and Brand A is the anchor item, Personalization recommends only items from Brand B.

This table includes the built-in exclusions and inclusions in Personalization.
You can also create a custom object in your catalog to use as an exclusion or
inclusion in Einstein Recipes. For more information, see [Create a Custom
Catalog
Object](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_custom.htm&language=en_US&type=5
"Personalization collects behavioral data in the context of the catalog that
you create and uses catalog objects to assess and analyze customer engagement
and affinities. You can add more detail to your catalog by using custom
objects. The more detailed you make your catalog, the more granular your
insights are regarding customer engagement and affinity.").

Exclusion or Inclusion | Description | Items Excluded or Included | Available When Recommending  
---|---|---|---  
Article | Filters articles to recommend or not recommend. | 

  * **Being viewed** : Item the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.
  * **From user attribute** : Value of the selected attribute.

| Articles  
Author | Filters by an author. | 

  * **Being viewed** : Items the customer is viewing.
  * **From explicit selection** : An item’s name or ID.

| Articles, blog posts, authors  
Blog post | Filters blog posts to recommend or not recommend. | 

  * **Being viewed** : Item the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID
  * **From user attribute** : Value of the selected attribute.

| Blog posts  
Category | Filters items in the same category as the current item. | 

  * **Being viewed** : Items the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.
  * **From user attribute** : Value of the selected attribute.

| Products, articles, blog posts, categories  
Class | Filters by an item’s classes. | 

  * **Being viewed** : Item the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.

| Products, item classes  
Compatibility | Filters tags or categories that are compatible or incompatible with the current anchor items. | Selected items the customer marked as favorites. You can configure Personalization to apply filtering based on a specified number of times and within a specified number of days an item is marked as a favorite. | Products, articles, blog posts  
Content class | Filters by a content class. | 

  * **Being viewed** : Item the customer is viewing.
  * **From explicit selection** : An item’s name or ID

| Articles, blog posts, content classes  
Department | Filters items in the same department as the current item.For example, instead of excluding or including within a category (like Men’s|Shoes), this option excludes or includes anything in the item’s department (like the entire Men’s department). | 

  * **Being viewed** : Items the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.
  * **From user attribute** : Value of the selected attribute.

| Products, articles, blog posts  
Favorited | Filters items a customer has marked as favorites. | Selected items the customer marked as favorites. You can configure Personalization to apply filtering based on a specified number of times and within a specified number of days an item is marked as a favorite. | All  
Gender | Filters by an item’s associated gender. | 

  * **Being viewed** : Item the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.
  * **From user attribute** : Value of the selected attribute

| Products, genders  
Inventory count | Filters items with an inventory count above, below, or between specified values. | 

  * **At least** : Items with an inventory count greater than the specified number.
  * **At most** : Items with an inventory count less than the specified number.
  * **In between** : Items with an inventory count within the specified range.

| Product  
Keyword | Filters by an item’s keywords. | 

  * **Being viewed** : Item the customer is viewing.
  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.

| Products, articles, blog spots, keywords  
Location | Filters items by their distance to the customer or to the item the customer is viewing.Location filtering uses latitude and longitude when determining distances to customers or items.  | 

  * **Item** : Items within the specified distance of the viewed item.
  * **User** : Items within the specified distance of the customer.

| All  
Price | Filters items according to various pricing aspects. | 

  * **Numeric** : Items greater than or less than a specified price, or between a specified price range.
  * **Percentage** : Items less than or greater than a percentage of a viewed item’s price.
  * **Cart value** : Items with a price that, when added to a partially filled cart, satisfy a specified cart price target.

| Product  
Product | Filters items to recommend or not recommend, based on specific settings or recent customer activity. | 

  * **In cart** : Items in the customer’s cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.
  * **From user attribute** : Value of the selected attribute.

| Products  
Product list | Filters items based on a static list you create. | 

  * **Being viewed** : Item the customer is viewing.
  * **In cart** : Items the customer has in their cart.
  * **Last purchased** : The most recent item the customer purchased.
  * **From explicit selection** : An item’s name or ID.
  * **From user attribute** : Value of the selected attribute.

| Products  
Purchased | Filters based on items the customer has previously purchased. | Selected items the customer purchased. You can configure Personalization to apply filtering based on a specified number of times and within a specified number of days items were purchased. | Products  
Rating | Filters based on items with an average rating that is above, below, or between specified values. | 

  * **Greater than** : Items with a rating greater than the specified value.
  * **Less than** : Items with a rating less than the specified value.
  * **Between** : Items with a rating within the specified range.

You can also include items that have no rating or a rating of zero. | All  
Recommended | Filters items a customer has previously received as recommendations. | Selected items the customer received as recommendations. You can configure Personalization to apply filtering based on a specified number of times and within a specified number of days recommendations were received. | Products, articles, blog posts  
Viewed | Filters items a customer has previously viewed. | Selected items the customer viewed. You can configure Personalization to apply filtering based on a specified number of times and within a specified number of days items were viewed. | All

