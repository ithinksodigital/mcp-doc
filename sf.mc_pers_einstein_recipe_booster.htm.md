

# Boosters in Einstein Recipes

Include boosters in Einstein recipes to boost items matching a customer’s
affinity in any recommendations Personalization presents.

## Booster Parameters and Affinity Scores

When you include a booster in an Einstein Recipe, Personalization incorporates
the customer's affinity score to boost items matching that affinity in the
recommendations it presents. The affinity score is based on a customer’s
interactions with your site, such as item views, items added to the cart, and
items purchased. For example, if a customer has a preference for a particular
category of item, Personalization shows items from that category first.

Each booster has three parameters that determine the affinity score.

Parameter | Description  
---|---  
Weight | Affects how much to weight the selected booster in the recommendation. The slider has five positions (1–5) that act as multipliers when factoring the affinity score.   
Lookback | The number of days to look back at a customer's history for the booster. For example, if a customer bought a product three months ago, and the lookback period is 30 days, Personalization doesn’t include that purchase when factoring the affinity score.  
Threshold | Determines the point at which the customer has an affinity for the booster. The slider has six positions (0–5) that act as multipliers when factoring the affinity score. If the threshold is zero, any of the items the user has interacted with during the lookback period are available to boost.  
  
## Boosters

Booster  | Description  | Available When Recommending   
---|---|---  
Authors | Personalization assigns a higher affinity score to the authors the customer shows an interest in. | Articles, blog posts  
Brand | Personalization assigns a higher affinity score to the brands the customer shows an interest in. | Products, articles, blog posts  
Category | Personalization assigns a higher affinity score to the categories the customer shows an interest in. This booster includes an option to boost a category hierarchy with decreasing magnitude. For example, if a category hierarchy is Women's|Dresses|Halter, Personalization also boosts items in the Women's|Dresses and Women's categories, but less than items in the full category. | Products, articles, blog posts  
Class | Personalization assigns a higher affinity score to the classes the customer shows an interest in. | Products  
Color | Personalization assigns a higher affinity score to the colors the customer shows an interest in. | Products  
Combination | Combination boosters allow more specific items to return as recommendations than when boosting by item type. These boosters determine which items the customer has an affinity for, and only boosts items with the same combination of categories and tags. You can combine up to three item types. If an item doesn’t have a value for a specific item type, Personalization doesn’t boost it.If a recipe has a category booster and a color booster, a customer who buys a red dress has an affinity for the color “red” and the category “dress.” So boosted recommendations are likely to be red, or dresses, but not necessarily red dresses. Because combination boosters only boost items with the specific combination of tags and categories, Personalization doesn’t boost red shoes and black dresses. As a result, those items are less likely to return as recommendations. | Products, articles, blog posts  
Content class | Personalization assigns a higher affinity score to the content classes the customer shows an interest in. | Articles, blog posts  
Department | Personalization assigns a higher affinity score to the departments the customer shows an interest in. | Products, articles, blog posts  
Gender | Personalization assigns a higher affinity score to the genders the customer shows an interest in. | Products  
Keyword | Personalization assigns a higher affinity score to the keywords the customer shows an interest in. | Products, articles, blog posts  
Product list | Personalization assigns a higher affinity score to product lists the customer shows an interest in. | Products, articles, blog posts  
Related information | This booster boosts a specific item type, such as category, based on the selected anchor item. When boosting a category, there’s also an option to boost through a category hierarchy with decreasing magnitude (see the category booster). | Products, articles, blog posts  
Store | Personalization assigns a higher affinity score to the stores the customer shows an interest in. | Products  
Style | Personalization assigns a higher affinity score to the styles the customer shows an interest in. | Products

