

# Create an Einstein Recipe

Einstein Recipes consist of ingredients, exclusions, inclusions, boosters, and
variations. Combine these components to suggest content or products according
to an individual customer’s behavior and affinities. Personalization uses your
recipes to create algorithms that present each customer with their own
personalized recommendations.

### Required User Permissions

Permissions Needed  
---  
To create an Einstein Recipe: | A role with Recipes Create/Edit permissions  
  
After you create an Einstein Recipe, use it in your campaigns to recommend
items based on what your customers have previously viewed or purchased.
Personalization’s predictive algorithms dynamically adjust to temporary shifts
in consumer behavior.

  1. In the **Machine Learning** section of the main navigation, click **Einstein Recipes**.
  2. Click **New Recipe**.
  3. Enter a **Name** for the recipe.
  4. Click **Recommendation Type** and select an item type from the dropdown.
  5. On the **Ingredients** tab, click **Add ingredient** and select an option from the dropdown.
  6. Select parameters for the ingredient.
  7. Add additional ingredients as necessary.
  8. Click **Additional Options** :
    1. If your recipe includes multiple ingredients and one of the anchor items isn’t present, you can select **Allow missing anchor item for multi-ingredient recipes**. This option presents recommendations from ingredients that either don’t require an anchor item or have fulfilled their anchor item requirements.
    2. To include trending items if the recipe doesn’t return any recommendations, select **Enable trending product fallback**. You can evaluate trending using a maximum setting of **Products from the past**`30` **days**.
  9. Click the **Exclusions** tab.
    1. Click **Add exclusion** and select an option from the dropdown.

![7696e2d0-51b0-46da-b09a-69a6b189dccf]

Note Options for exclusions and inclusions vary according to the
Recommendation Type you select. See [Exclusions and Inclusions in Einstein
Recipes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_recipe_exclusion_inclusion.htm&language=en_US&type=5
"Use exclusions and inclusions to add filtering criteria to your Einstein
Recipes to control which items to recommend to your customers. For example,
you can add an exclusion to show only items from the same category as the item
a customer is viewing. A customer who views a specific hat brand only sees
recommendations for other hats, and not items from the same brand.").

    2. To use the selected option as an inclusion, click **Include**.
    3. Select parameters for the exclusion or inclusion.

![74d3dec1-1163-4e2d-93d7-dd8e6854fcec]

Note If you select the **Enable trending product fallback** option for an
ingredient or for the campaign, Personalization can recommend an exclusion if
that excluded item is trending.

    4. Add additional exclusions or inclusions.
  10. Click the **Boosters** tab.
    1. Click **Add booster** and select an option from the dropdown.

![66d6736c-eba4-4e9b-933b-a86e54894ade]

Note Options for boosters vary according to the Recommendation Type you
select. See [Boosters in Einstein
Recipes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_recipe_booster.htm&language=en_US&type=5
"Include boosters in Einstein recipes to boost items matching a customer’s
affinity in any recommendations Personalization presents.").

    2. Select parameters for the booster.
    3. Add additional boosters.
  11. Click the **Variations** tab.
    1. Click **Add variation** and select an option from the dropdown.

![fd99b2b0-70f9-4e43-ab7b-7eb0a0ff5395]

Note Options for variations vary according to the Recommendation Type you
select. See [Variations in Einstein
Recipes](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_recipe_variation.htm&language=en_US&type=5
"Use variations in Einstein Recipes to modify the recommendations that
Personalization presents so that your customers see a wider array of items.
For example, you can configure a variation to force a recipe to show at most
two items from the same category. So if a customer has an affinity for the
"hats" category, Personalization recommends the two most relevant hats and a
variety of other items from different categories.").

    2. Select parameters for the variation.
    3. Add additional variations as necessary.

![c60a29c4-6117-4eb2-a405-0e6c6232162f]

Note You can add only one dimensional and one randomized variation per recipe.

  12. Save your work. 

![b43a67b4-83a6-4e4d-adf4-44af45fc6036]

Note Your recipe must have a unique name and at least one ingredient before
you can save it.

  13. To compile the algorithms that Personalization uses to present recommendations, click **Train**.

Each night, Personalization automatically retrains live recipes that are
actively in use. Active recipes are ones that Personalization has used in the
past week. Depending on your dataset and customer base, training can take
several hours.

  14. When you’re finished creating and training a recipe, be sure to test it before publishing it.

