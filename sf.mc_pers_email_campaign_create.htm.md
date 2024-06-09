

# Create an Open Time Email Campaign

Generate a block of HTML code for an Open Time Email campaign and use it in
your existing email marketing service to add personalized content for each
recipient. After creating an Open Time Email campaign, you can clone it and
reuse it with the same recipe for additional campaigns. You can also add
exclusions and inclusions to your campaigns to tailor them to your overall
email strategy.

### Required User Permissions

Permissions Needed  
---  
To create an Open Time Email campaign: | A role with Campaign Create/Edit permissions  
  
To create an Open Time Email campaign that uses recipe-driven recommendations,
you must design an open time item template that controls how content and
product recommendations display in that campaign.

The process of creating an Open Time Email campaign determines how many images
to render, and which recommendation strategy to apply for each content block
in the campaign.

  1. In the **Channels & Campaigns** section of the main navigation, select **Email** | **Open Time Campaigns.**
  2. Click **New Campaign**.
  3. Enter a **Campaign** | **Name**.
  4. Enter a **Name** for the first content block.
  5. Select an option from the **Item Type** dropdown, such as **Product** or **Brand**. The options depend upon your dataset.
  6. Select **Display Block Title** if you want to add a title to the content block.
  7. Enter the title to display at the top of the content block.
  8. Make any necessary adjustments in **Edit Title CSS** to style the title.
  9. Select an **Item Template** and then configure:

Item | Description  
---|---  
**Block Size** | Height and width of the block, in pixels  
**Number of Items** | Number of items to include in the block  
**Block CSS** | CSS around all the items  
**Item Wrapper CSS** | CSS for the template wrapper  
**Image Alt Text** | Text that describes the image for users who are unable to see it  
  
![366989c3-d618-4f1c-92d8-0bd58d6dd470]

Note The list of available item templates depends on the Item Type that you
select in step 5.

  10. To hide the content block, select the **Hide Block for This Experience** option.

![7616bbf1-6e3c-497f-89e2-57ebfe7a7a58]

Note Hide a content block when you want to test an experience that doesn’t
contain certain content against one that does.

  11. Select **Recipe** as the **Promotion Type** and then **Select a Recipe** from the list of your existing recipes.

![48518314-89a5-4887-8c36-47b9b75bf3db]

Note On-page anchor item exclusion recipes and on-page anchor items used to
show recommendations are not compatible with Open Time Email.

  12. If you don’t want to add trending items to recommendations blocks that don’t return results, select **Disable Trending Fallback**. 
  13. To add an exclusion, click the **Add exclusion** dropdown and select an option from the list.
  14. Select **Exclude** or **Include** as necessary and make any other applicable selections from the available parameters.

![66483924-4f69-458a-b9f4-46426b8c8a9d]

Note Adding exclusions and inclusions at the campaign level, rather than
within a recipe, lets you reuse the same recipe for multiple campaigns.

  15. Add any additional exclusions or inclusions.
  16. Save your work.
  17. Click **Add new block** to create another block with a different recommendation strategy. Adding different experiences allows you to target different audiences with the same campaign details.
  18. To test your campaign and confirm that the recommendations render in the email environment as you expect, click **Simulate**.
  19. Personalization selects a user and populates the corresponding recommendations. You can copy and paste a user ID into the dropdown to test recommendations for other specific users.

![d8f317fe-a32e-4f7f-9705-f2b7970312fb]

Note The simulator uses a cache-buster, which means it generates a new call
every time you select a user. So it’s possible to see a different image in the
simulator than in the actual email.

  20. Click **X** to close the dialog.
  21. If you’re done creating your campaign and ready to publish it, click Save and Close.

After you create your Open Time Email campaign in Personalization, you
generate HTML code to insert into an email campaign in your email marketing
system. When recipients open their emails, the Open Time Email HTML code
delivers personalized recommendations.

