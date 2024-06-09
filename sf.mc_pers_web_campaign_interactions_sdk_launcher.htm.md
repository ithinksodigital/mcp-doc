

# Install the Salesforce Interactions SDK Launcher

Install the Salesforce Interactions SDK Launcher, a Google Chrome browser
extension, which includes the Visual Editor. You use the Visual Editor to add
personalization features to your website. Using web campaign templates, you
can create personalization campaigns targeted to specific groups, individual
users, or events.

### Required User Permissions

Permissions Needed  
---  
To install the SDK: | A role with Administrator permissions  
  
The Salesforce Interactions SDK Launcher supports only the UTF-8 charset.

Remove any previously installed Evergage extensions, such as the Evergage
Visual Editor and Evergage Launcher, before installing the SDK Launcher.

![890f667e-07b7-48f3-9e85-5c29c3f9560f]

Note You currently can’t use the Visual Editor and Google Tag Manager (GTM)
simultaneously. GTM interferes with the Visual Editor by overwriting button
functionality and causing refreshes. We’re investigating a workaround. If you
encounter issues, check to see if you have GTM installed. If so, contact
Google's GTM support team for help with disabling it.

  1. Open Google Chrome and navigate to chrome://extensions/.
  2. Navigate to the [Salesforce Interactions SDK Launcher Chrome store page](https://chrome.google.com/webstore/detail/salesforce-interactions-s/mhmpepeohaddbhkhecaldflljggicedf?hl=en#:~:text=Salesforce%20Interactions%20SDK%20Launcher&text=Provides%20support%20for%20launching%20either,Visual%20Editor%20on%20any%20domain).
  3. Click **Add to Chrome**.
  4. From the popup dialog that appears, click **Add extension**.
  5. Log in to Marketing Cloud Personalization.
  6. Click the avatar icon at the top right and select **Manage Datasets** from the menu that appears.
  7. Click **+Dataset**.
  8. Enter a unique identifier, such as “sfsdk,” in the **ID** field.
  9. Enter a display name in the **Name** field, such as “Salesforce Interactions SDK Launcher.”
  10. Click **OK**.
  11. Navigate to your website.
  12. Click the **Extensions** icon in your browser’s toolbar and select **Salesforce Interactions SDK Launcher**. 
  13. “Interaction Studio & Salesforce CDP” appears in the **Product Type** dropdown. If it doesn’t, select it.
  14. The dialog displays the following information for your website:

Setting | Description  
---|---  
**Detected Beacon** | A green check indicates that the Marketing Cloud Personalization JavaScript Beacon is installed. The associated account, associated dataset, and beacon version appear below it.  
**Account** | The name of the account associated with the installed Personalization JavaScript Beacon. Typically, your account name is your company or brand name.  
**Dataset** | The name of the dataset associated with the installed Personalization JavaScript Beacon. You can have only one dataset for your account, or you can have multiple datasets. For example, you can have a dataset for different sites that are based on brand or geography. You can also have datasets for staging and production.  
  
  15. If there’s an orange X next to **Detected Beacon** , the Personalization JavaScript Beacon isn’t installed. To install it, follow these steps:
    1. Enter the account name in the **Account** field.
    2. Enter the name of the dataset in the **Dataset** field.
    3. Turn on the **Inject SDK** option.
    4. Refresh the page.
    5. Click the **Extensions** icon in your browser’s toolbar and select **Salesforce Interactions SDK Launcher**. 
    6. Confirm that a green check appears next to **Detected Beacon** , the correct account and dataset appear in the applicable fields, and the orange **Injected** indicator appears beside the beacon version. 

![38d22418-2a65-4f78-9c92-dac61eb4cfca]

Note Cached data can cause issues in your browser. If you don’t see the
updated settings, try refreshing the page a few times. If problems persist
with beacon detection or SDK injection, try uninstalling and reinstalling the
Salesforce Interactions SDK Launcher.

  16. Turn on the **Visual Editor** option.
  17. List your website domains on the allowlist. For more information, see [Add Domains to the Visual Editor Allowlist.](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_visual_editor_allowlist.htm&language=en_US&type=5 "You can use the Visual Editor only with website domains that you include on the Allowed Domains list. If you don’t list your domains on the allowlist, you can’t log in to the Visual Editor.")

![c12990cc-97a2-4b5b-a038-b3984ef41e78]

Note You can use the Visual Editor only with website domains on the Allowed
Domains list. Otherwise, you can’t log in to the Visual Editor.

#### See Also

  * [Add Domains to the Visual Editor Allowlist](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_visual_editor_allowlist.htm&language=en_US&type=5 "You can use the Visual Editor only with website domains that you include on the Allowed Domains list. If you don’t list your domains on the allowlist, you can’t log in to the Visual Editor.")

