

# Test an Einstein Recipe

After creating and training an Einstein recipe, make sure to test it before
you publish it. Using test groups can simulate the recommendations that
Personalization presents to a group of customers. Testing your recipe with
groups that have varying behaviors and affinities helps ensure optimal
customer experiences.

### Required User Permissions

Permissions Needed  
---  
To test an Einstein Recipe: | A role with Recipes Create/Edit permissions  
  
Using the recipe simulator, you can test your Einstein Recipe with
Personalization’s sample test group or create your own.

![a80f841c-8bea-447f-b72b-3f795a0eb022]

Important The recipe simulator provides guidance and displays items that
Personalization potentially recommends to customer groups. The simulator
doesn’t reflect the actual recommendations in Personalization production.
Simulated recommendations aren’t updated in real time.

  1. In the **Machine Learning** section of the main navigation, click **Einstein Recipes**.
  2. Find your recipe and click **Edit**.
  3. To test your recipe with Personalization’s sample test group, click **Simulate** next to **Sample Test Group**. The simulator opens in a new browser tab and displays the recipe’s recommendations for each test group customer in the **Simulation** section.

![f34131d7-83c6-4e6c-be6f-2c87acfa5c44]

Note The information in this section updates automatically when you make a
change, resimulate the test, reload the page, or select a test group with at
least one user.

  4. To view the unified customer profile for a customer, click a customer ID.
  5. To view a scrollable list of a customer's purchase history, click the amount beside a customer ID. 

![2dffbd63-4340-42de-b1c8-1888b951f56d]

Note You can’t click purchases with a value of 0.

  6. To view the current contents of a customer's shopping cart, click the shopping cart icon. 

![bff77582-6bfd-41cb-91f3-1c2242b7d81d]

Note This icon doesn’t appear when the customer's cart is empty.

Audience attributes appear below each customer ID: For Random users,
attributes match the filters you set in the audience filtering section; for
Specific users, attributes reflect the customer's current behavior. Item
affinities appear for each customer. Green represents purchase data and blue
represents visit data.

  7. To replace a random user, click the dice icon.
  8. Click a recommended item image to open a popup with additional options. For example, to view a recommended item on your website, click the open page icon, to open a recommended item for editing in your Personalization catalog, click the catalog icon.
  9. Click the **Sample Test Group** name at the top and enter a name for this test scenario.
  10. To modify the test group, expand the **Add Users to Test Group** section and use the search field and audience filters. Personalization displays four additional customers and a random user that meet the recipe’s criteria. To add any of these customers to the test group, click its plus sign.

![4bdd86ca-992c-4b38-adb4-8e124223b009]

Note Test groups can contain a maximum of 20 customers.

Option | Description  
---|---  
Search by name, email, or ID | To find a specific customer to add to the test group, enter a name, email, or user ID in the search field. Select the desired customer from the list and click the plus sign to add them to the group.  
Search users by audience filtering | Select one or more of the audience options to find and add customers who match that criteria. The four additional customers that display change as you make selections.The options that appear depend on whether your site has revenue tracking enabled.To clear a row, select an option and click to the left of the row.  
Select segments | To add segment filters, select one or more segments of customers.  
Clear all filters and conduct new search | Click **Clear filters and search for another user by audience** to clear all selected filters so you can conduct a new search, then save after modifying the test group.  
Test the recipe | Click **Resimulate** to test the recipe with the modified test group.  
  
  11. To test other recipes, click the **Recipe** dropdown in the **Test Configuration** section, select the desired recipe, and click **Resimulate**.

![011ef79f-375d-4e63-a30f-11ff5fb391b8]

Note If you have an unpublished version of a recipe, you can select it or the
live version.

  12. To test other anchor items, click the current anchor item, begin typing an item name, select the desired item from the list, and click **Resimulate**. 
  13. To view an item on your website, click the open page icon.
  14. To open an item for editing in your Personalization catalog, click the catalog icon.
  15. To view the statistics for a product in Personalization, click the detail icon to open the Product Detail page.
  16. When you’re done testing, click **Save** and then **Close**.
  17. To finalize your recipe and make it available to use in campaigns, click **Publish**.

![c716fc22-156f-431e-850c-8dcf38010d31]

Note After you publish a recipe, any edits you make don’t take effect until
you publish it again.

  18. To create your own test group, click **Create Test Group** and use the parameters described previously.

![0a3de45d-1ced-497f-9504-23e75deb0587]

Note You can have up to 15 test groups, including the sample test group.

#### See Also

  * [ _Video_ : How to Test an Einstein Recipe in Recipe Simulation](https://youtu.be/QUCCbvLvv6s)

