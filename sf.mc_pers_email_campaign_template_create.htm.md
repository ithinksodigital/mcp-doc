

# Create an Open Time Item Template

Create open time item templates, which are used with content blocks, to define
the layout for recommendations in a recipe-driven Open Time Email campaign.

### Required User Permissions

Permissions Needed  
---  
To create an open time item template: | A role with Item Template Create/Edit permissions  
  
Be sure that you have products in your catalog and trained recipes to use in
your campaigns. Familiarity with HTML can help you create an open time item
template that matches your company’s branding.

An open time item template controls how content and recommendations display.
Templates render as images to ensure that they display consistently,
regardless of email service provider or viewing device.

  1. Go to **Channels & Campaigns** and select **Email** > **Open Time Item Templates**.
  2. Click **New Item Template**.
  3. Enter a **Name** for the template.
  4. Select the **Item Type** to display inside the open time item template, such as **Product**. The options depend upon your dataset.
  5. Enter the template **Dimensions** (width and height in pixels).

![9f593035-e5d1-4319-a3ce-07dad2ae7d6c]

Note You’re defining the content block for a single image or item not a row or
grid of items. When you build an email campaign, you can add additional rows
(as sections) and items.

  6. Define the template by adding HTML code that you want to apply to each item in your catalog. 

The following HTML sample renders a product image (260 x 375 pixels) above the
product name with a suggestion to "Shop now" at the bottom. The item template
uses dimensions of 280 x 500 pixels.

![8e2009fe-71fd-4761-92c7-ffe1bb868410]

Note When defining HTML content for your open time item template, confirm that
images of different dimensions and names of varying lengths render as you
intend.

    
        <div style="padding: 10px; font-family: Arial, 'Helvetica
            Neue', Helvetica, sans-serif; font-size: 20px;">
              <div style="width: 260px; height: 375px;">
              <img src="${item.imageUrl}" style="max-width: 100%;
            max-height: 100%;">
              </div>
              <!-- allocate enough height for 3 lines of text -->
              <div style="margin-top: 15px; height:
            70px;">${item.name}</div>
              <div style="font-weight: bold;"><span
            style="text-decoration: underline;">Shop now</span> ></div>
              </div>

  7. To add dynamic message content fields to the HTML code, place your cursor in the desired location of the code, click **Insert Dynamic+** , and select an option. To change how the content renders in your email campaign, adjust the HTML around the dynamic fields. 

![f206a8d1-34c4-4146-b0a4-9ebf6d089e6d]

Note Advanced Dynamic Message Content (ADMC) syntax is also supported. ADMC
provides greater flexibility and control over dynamic message content. For
more information, see [Salesforce Developer Documentation: ADMC
Reference](https://developer.salesforce.com/docs/marketing/personalization/guide/advanced-
dynamic-message-content.html).

  8. To preview the open time item template, click **Refresh Email Preview**.

![e1fb6de3-efb7-4ddd-8ffd-f33b2ad723f8]

Note When you publish an open time item template, Personalization generates
the images for every item in your catalog, which can take a significant amount
of time. Use the preview feature to see how the template renders before
publishing it.

  9. Make any necessary adjustments and save them.

![fe9b0675-7bab-4e90-ae95-71b3b843497e]

Note You can’t change an open time item template after you publish it.

When you finish creating the open time item template, follow the steps in
[Publish Open Time Item
Templates](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_template_publish.htm&language=en_US&type=5
"Publish open time item templates to define a layout for recommendations in a
recipe-driven Open Time Email campaign.") so you can use it in an email
campaign.

