

# Replace the SDK URL Locally

If the Server-Side JavaScript beacon is already present on your site, you can
change the dataset used on the site in your local browser with the Force SDK
URL option. This option is useful if you want to work on a different dataset,
for example, to maintain a development or testing dataset and a live
production dataset.

### Required User Permissions

Permissions Needed  
---  
To install the SDK: | A role with Administrator permissions  
  
  1. In the Personalization Managed Datasets dropdown list, select the dataset you want to use.
  2. In the left navigation, select **Web** > **JavaScript Integration**.
  3. On the **Synchronous** tab, copy the value for **src** and append it to https: to create a URL in the format: https://cdn.evgnet.com/beacon/account/dataset/scripts/evergage.min.js

Make note of this URL as you’ll use it later in Step 8.

  4. Navigate to your website (for example, northerntrailoutfitters.com).
  5. Click the **Salesforce Interactions SDK Launcher Extension**.
  6. Enter the account and dataset (for example, account = training and dataset = nto).
  7. On the **Advanced** dropdown at the bottom of the browser extension window, turn on **Force SDK URL**.
  8. Add the SDK URL that you created in Step 3 (For example, https://cdn.evgnet.com/beacon/training/nto/scripts/evergage.min.js).
  9. Refresh the page.
  10. Click **Salesforce Interactions SDK Extension**.
  11. Confirm that a green check appears next to Detected Beacon and that the correct account and dataset appear in the designated fields. 

![d935f0a3-cc83-4292-94d6-85b395b2bee2]

Note Due to cached browser data, you might need to refresh the page several
times to see the new settings.

