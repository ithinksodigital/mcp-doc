

# Troubleshoot an Einstein Recipe

Examine Einstein recipes and unified customer profiles if you run into
unexpected recommendations. Einstein Recipes can consist of multiple
components with a variety of parameters. The algorithms are complex, and some
recipe options can conflict with one another. Any initial recommendations you
receive can require some fine-tuning to meet your expectations.

## Examine the Recipe

Start by examining the recipe’s construction. Verify that the setup of each
ingredient, exclusion, inclusion, booster, and variation is as you intend. The
maximum number of items that a web template can return is 12, however, your
developer can configure a template to return fewer than 12 items. If the
recipe doesn’t display any recommendations, there are several things to check.

What to check... | Considerations...  
---|---  
What ingredients are included in the recipe? | If you add an ingredient that requires an on-page anchor item, such as the co-buy ingredient, you must enter a sample item name or ID as the anchor item. As you enter different item names or IDs into the **Anchor Item** field, the recipe presents different recommendations according to what the customer is viewing on the page.  
Is the anchor item presenting recommendations? | If you create the recipe with an ingredient that requires an anchor item, the recipe training could lack enough data for that anchor item. For example, if you train a Co-Buy ingredient, customers that bought the anchor item must buy enough other items enough times during the lookback period to see recommendations. If an ingredient in the recipe requires an in-cart or last-purchased anchor item, find a customer with an open cart or a recently purchased item. If the recipe doesn’t already include a fallback ingredient, try adding either the trending or collaborative filtering ingredient as a fallback. Then retrain the recipe and resimulate it to see if it presents recommendations.  
Is there an exclusion in the recipe? | Exclusions always override inclusions, so if there’s a conflict, the exclusion always wins. Check for conflicting exclusions and inclusions that prevent the recipe from suggesting recommendations.  
Is the expected item promotable? | Is the expected item promotable? Certain items don’t appear as recommendations unless they meet all necessary criteria. For example, if there’s a published date, the current date must be after it. If there’s an expiration date, the current date must be before it. For products, there are additional criteria. Each product must have a value for the following item attributes: ID, name, URL, image URL, and a price greater than zero. Any product inventory counts must be greater than zero.  
  
## Examine the Unified Customer Profiles

If the recommendations still don’t meet your expectations after examining the
recipe components, review the unified customer profiles of the customers
you’re using to simulate the recipe. Look at each customer’s affinities and
data to determine whether the recommendations make sense based on each
customer’s data.

Research a customer’s affinities by views, view times, and purchases. Also
review information about their segment memberships, action details, and
affinity details. Try a few specific boosters and review the recommendations
they provide.

Booster | Description  
---|---  
Category booster | This booster can help verify whether the recommendations make sense based on a customer’s category affinities.  
Related information booster | This booster can help verify whether the recommendations agree with a customer’s affinities for particular item types.  
  
Repeat this process with as many customers as needed for you to understand the
recommendations you receive.

## Methodically Test the Recipe

If you’ve researched the unified customer profile for each customer and still
aren’t satisfied with the recommendations, start over and test each component
as you create the recipe.

Remove all ingredients, exclusions, inclusions, boosters, and variations. Then
add one recipe component at a time and use the recipe simulator to view the
resulting recommendations. Review the unified customer profiles as you test
each component.

By methodically testing each component, you can uncover the one responsible
for the recommendations that don’t meet your expectations.

