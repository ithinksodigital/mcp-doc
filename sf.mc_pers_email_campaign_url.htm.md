

# Capture Open Time Email Campaign URLs

Use URLs from Open Time Email campaigns to import item images or link to
catalog items in externally-managed email campaigns. For some email marketing
services, you can use only the URLs from your Open Time Email campaign, and
not the entire HTML code block generated using Personalization.

### Required User Permissions

Permissions Needed  
---  
To capture a URL: | A role with Campaign Create/Edit permissions  
  
Create an Open Time Email campaign and generate the block of HTML code that
you use in your existing email marketing service to add personalized content
for each recipient.

Rather than copy all the generated HTML code, you can select specific URLs and
embed them in your email template.

  1. In the **Channels & Campaigns** section of the main navigation, select **Email** | **> Open Time Campaigns. **
  2. Select the email campaign and click **Edit**.
  3. Click **Simulate**.
  4. Click **Show HTML**.
  5. To resize the HTML window, use the resize handle at the bottom right.
  6. Locate the <a> and <img> tags for each content block in the HTML code. The <a> tag indicates an item, and the <img> tag indicates an image.
  7. Copy the URL from within each tag and replace:
    1. The number in the middle section of the URL (such as /1/) with the item’s product number.
    2. The value after ?userId= with the unique ID of the recipient.

![de66863a-be70-44dd-8196-b031cd8fa5d2]

Note The string after ?userId= is for simulation purposes only so don’t copy
it into the email template in your email marketing service.

  8. Insert the modified URLs into your email campaign where necessary.
  9. When you finish, click **X** to close the **Simulating** dialog in Personalization.
  10. To see sample HTML and the URLs to copy from it, refer to the developer documentation article for [Capture an Open Time Email Campaign URL](https://developer.salesforce.com/docs/marketing/personalization/guide/capture-email-campaign-url.html?q=email%20campaign).

