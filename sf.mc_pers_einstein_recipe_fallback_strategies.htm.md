

# Fallback Strategies

Fallback techniques can enhance your Einstein recipe-building strategy and
ensure that a recipe returns enough items to fill the recommendation slots
designated by a campaign.

This table lists possible fallback options to use, their benefits, and things
to consider when using them in a recipe.

Fallback | Benefits | Considerations  
---|---|---  
Any Eligible Item ingredient | 

  * Acts as a fallback for other ingredients.
  * If there isn’t enough user data to provide a full list of recommendations, this ingredient includes items that meet the minimum data requirements for the target recipe.
  * Populates only enough recommendations to meet the minimum number of promoted items for the campaign.
  * Compatible with all other ingredients.
  * Eligible items obey existing exclusions, inclusions, and variations.

|

  * For a product to be recommended, it must meet the minimum requirements (name, ID, URL, image URL, price, and an inventory of null or not zero).
  * If the recipe doesn’t include exclusions, inclusions, or variations, this ingredient returns a random set of items.

  
Collaborative Filtering ingredient | 

  * Has trending built in.
  * Defaults to showing trending results when there’s no user or item activity during the configured lookback period.
  * Trending results are identical to using a Trending ingredient with a weight value of 1.
  * Eligible items obey existing exclusions, inclusions, and variations.

|

  * Built-in trending fallback applies only to the collaborative filtering ingredient.
  * You can’t customize trending parameters. Trending is hard-coded to recommend products by most purchased and recommend other catalog objects by most viewed.
  * The trending in Collaborative Filtering ingredients stacks with Trending ingredients in recipes. This stacking is equivalent to having multiple trending ingredients in the recipe, each with potentially different weights. In recipes containing three or more ingredients, and no user or item activity has occurred within a specified lookback period, stacked Trending ingredients can overpower other ingredients in the recipe.

  
Trending ingredient | 

  * Enables setting a trending weight (1–4) using a graduated slide.
  * Eligible items obey existing exclusions, inclusions, and variations.
  * Recommends products by most revenue, most purchased, most time spent viewing, or most viewed.

|

  * Provides trends using statistics from only the past 24 hours.
  * No configurable lookback period.

  
Enable trending product fallback option | 

  * Checkbox works for the entire Einstein recipe.
  * Populates only enough recommendations to meet the minimum number of promoted items for the campaign.
  * Enables you to evaluate products for trending over a specified number of past days. The maximum setting for evaluation is for products from the past 30 days.

|

  * Shows trends only by purchase count for products and view count for other catalog objects.
  * Ignores exclusions, inclusions, and variations.

  
  
## Precautions for Email Campaigns

When using a recipe in an email campaign, the system checks whether the email
contains blank recommendation slots. By default, all Open Time email requests
perform a Trending lookup (by views over the past week) to fill empty slots
with items. If you don’t want to show recommendations in an Open Time email,
you can override the default behavior. On the item block, deselect Enable
trending product fallback for the recipe.

The Trending lookup used by an Open Time email request ignores inclusions,
exclusions, and variations.

