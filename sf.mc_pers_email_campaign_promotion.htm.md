

# Use Promotions in Email Campaigns

Tailor email campaign experiences for each recipient using promotions, without
using different copy or separate recipient segments. For each promotion, you
can view detailed statistics, so you know what's working and can adjust what
isn't. After you create a promotion, you can add it to an Open Time Email
campaign. You can use the same promotion across multiple campaigns and
experiences. For example, in one campaign, you can create a different
experience for tablet, phone, and desktop users.

### Required User Permissions

Permissions Needed  
---  
To use promotions: | A role with Catalog Create/Edit permissions  
  
  1. In the **Channels & Campaigns** section of the main navigation, select **Email** | **Open Time Campaigns**.
  2. Click **New Campaign**.
  3. Enter a **Name** for the block.
  4. Select **Promotions and Actions** as the **Item Type**.
  5. Select a **Promotion Type**.

Promotion Type | Description  
---|---  
**Static** | Displays the same asset within the campaign experience. After you select the static promotion for your email, select the corresponding asset to display. Only assets with an assigned content zone or tag appear as options.  
**Dynamic** | Displays the promotion to the recipient based on validity and eligibility criteria. If a recipient is eligible for multiple promotions that share the targeted content zone or tag, Personalization randomly selects a promotion from that set.  
**Decisions** | Use Einstein Decisions machine learning to select the optimal promotion for the recipient.  
  
![cc4dadf8-16db-41e9-a00e-7186d7f241f3]

Note To use dynamic or decisions-based promotions, you must designate the same
content zone or tag for each promotion on their individual **Assets** tabs.
For more information, see [Add Assets to a
Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_asset_add.htm&language=en_US&type=5
"For a promotion to appear in a campaign, it must have an associated asset,
such as an uploaded image or a URL that points to an external image.").

  6. Select the associated options for the Promotion Type.
  7. If you want to add additional item blocks to your email campaign, click **Add New Block**. 
  8. To add another experience that you can configure for different recipients of the same campaign for rule-based or A/B testing, click the blue plus sign beside the Experience 1 tab.
  9. Enter a **Campaign Name**.
  10. Save your work.

![2e4080ad-5b42-4698-9b34-8df26d5214b6]

Note Make sure that you have eligible campaigns by the time your campaign is
live. Make sure that you update expired promotions as well as include eligible
promotions in your campaigns.

#### See Also

  * [Campaign Promotions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion.htm&language=en_US&type=5 "Offer your customers special deals or advertise specific products with campaign promotions in Marketing Cloud Personalization. A promotion is an image that encourages customers to click through for more details. You can deploy promotion images on a web page or in an email, including call-to-action messages or incentives to engage customers and achieve specific business goals. You can also use promotions with Einstein Decisions for rule-based decisions and machine learning to target customers in multiple channels.")
  * [Einstein Decisions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_decision.htm&language=en_US&type=5 "When a user views a promotion on your website, Marketing Cloud Personalization captures the user's context—including whether they’re a returning visitor, the device they’re using, and other information that provides insight into that user. Einstein Decisions, Personalization’s machine learning approach for next-best-offer decisioning, uses that context to predict the value of showing a specific offer to a particular user.")
  * [Create an Open Time Email Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_create.htm&language=en_US&type=5 "Generate a block of HTML code for an Open Time Email campaign and use it in your existing email marketing service to add personalized content for each recipient. After creating an Open Time Email campaign, you can clone it and reuse it with the same recipe for additional campaigns. You can also add exclusions and inclusions to your campaigns to tailor them to your overall email strategy.")

