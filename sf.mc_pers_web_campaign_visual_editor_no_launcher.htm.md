

# Access the Visual Editor Without the Salesforce Interactions SDK Launcher

If your organization doesn’t allow you to download and install Chrome
extensions, you can access the Visual Editor by launching it from within
Marketing Cloud Personalization.

### Required User Permissions

Permissions Needed  
---  
To configure the Visual Editor: | A role with Configure Dataset permissions  
  
![f228cdd0-3545-4b06-9272-0a4308a32638]

Note You can use the Visual Editor only with website domains that you include
on the Allowed Domains list. If you don’t list your domains on the allowlist,
you can’t log in to the Visual Editor.

  1. Select the desired dataset from the Marketing Cloud Personalization menu bar.
  2. From the **Channels & Campaigns** section of the main navigation, select **Web > Website Configuration**.
  3. On the **Allowed Domains** tab, click **+New Domain**.
  4. Enter the domain name of your website, such as northerntrailoutfitters.com.

![dd6c2823-7266-4ed7-91be-0799b9b7bbb4]

Note Don’t include the HTTPS protocol, wildcards, or slashes in the name.

  5. To include all subdomains on the allowlist, set **Include Subdomain** to **true**.
  6. Click **Save**.
  7. Repeat the process for your other datasets.
  8. Click the **Install and Launch** tab.
  9. Enter the full URL of your website where the Personalization Javascript Beacon is deployed, such as https://www.northerntrailoutfitters.com.

![c332b2c0-586f-4420-8f61-d29cb51b482e]

Note Be sure to include the HTTPS protocol in the URL.

  10. Click **Save**.
  11. If your Personalization Javascript Beacon points to multiple websites from a single dataset, click **Add New Site** and add the other website URLs.
  12. To launch the Visual Editor, click **Launch**. The Visual Editor opens in a separate tab.

#### See Also

  * [Add Domains to the Visual Editor Allowlist](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_visual_editor_allowlist.htm&language=en_US&type=5 "You can use the Visual Editor only with website domains that you include on the Allowed Domains list. If you don’t list your domains on the allowlist, you can’t log in to the Visual Editor.")

