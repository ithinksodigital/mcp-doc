

# Manual Promotion Selector Web Campaigns

Create a web campaign using your existing promotions. Use the built-in global
template or use a custom template that a developer creates.

## Prerequisite

Before you create a manual promotion selector web campaign, you must enable
the Promotions feature and create a promotion. For more information, see
[Create a
Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_create.htm&language=en_US&type=5
"Create a campaign promotion to offer special deals and promote specific
products. When creating a promotion, the only required information is the name
and the URL of the landing page. For a promotion to return in a campaign, you
must have an asset associated with the promotion. Adding eligibility criteria,
promotion attributes, and related catalog objects is recommended. A promotion
attribute determines which promotions appear in a campaign. Personalization
uses related catalog objects to track and measure customer affinities across
item types in your catalog.").

## Manual Promotion Selector Web Template

The manual promotion selector web template uses assets in your promotions. If
a promotion asset references an external image URL, you must ensure that the
URL doesn’t change. If the URL changes or if you delete the asset, the
campaign doesn’t display correctly.

The manual promotion selector web template available to you can differ in name
and configuration options due to modifications by your developer. If you need
additional styling or configuration options, ask your template developer about
modifying the template.

**Manual Promotion Selector** —Select this template to create a web campaign
using your existing promotions.

Option | Description  
---|---  
**Content Zone** | Available content zones appear in this dropdown. If your developer selected a single content zone, there isn’t a content zone dropdown. If you need another content zone, ask your developer to modify the template.   
**Promotion Selector** | Search for the promotion you want to display in the content zone by typing the name of the promotion and then selecting it from the list that appears.   
**Asset Selector** | Select the promotion’s asset you want to display in the content zone.

