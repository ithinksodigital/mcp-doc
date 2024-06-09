

# Einstein Decisions Web Campaigns

You can use the Einstein Decisions machine learning algorithms to create next
best offers for your web campaign. Use the built-in global template or a
custom template that a developer creates.

### Required Editions

Available in: Premium Edition  
---  
  
## Prerequisites

Before you create an Einstein Decisions web campaign, you must:

  * Enable the Promotions feature and create a promotion. For more information, see [Create a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_create.htm&language=en_US&type=5 "Create a campaign promotion to offer special deals and promote specific products. When creating a promotion, the only required information is the name and the URL of the landing page. For a promotion to return in a campaign, you must have an asset associated with the promotion. Adding eligibility criteria, promotion attributes, and related catalog objects is recommended. A promotion attribute determines which promotions appear in a campaign. Personalization uses related catalog objects to track and measure customer affinities across item types in your catalog.").
  * Configure the Einstein Decisions Feature Engineering options. For more information, see [Feature Engineering in Einstein Decisions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_decision_feature_engineering.htm&language=en_US&type=5 "Feature engineering refers to the process of selecting features to use in a machine learning model. A feature is a data type that the model can observe and include in its training. To determine which data Einstein Decisions references, you define the machine learning features on the Feature Engineering page.").

## Einstein Decisions Web Template

The Einstein Decisions web template available to you can differ in name and
configuration options due to modifications by your developer. If you need
additional styling or configuration options, ask your template developer about
modifying the template.

Select this template to create a machine learning-driven next-best-offer
campaign.

Field | Description  
---|---  
Content Zone | Available content zones appear in this dropdown. If your developer selected a single content zone, there isn’t a content zone dropdown. If you need another content zone, ask your developer to modify the template. Only promotions with assets mapped to the targeted content zone are available.  
Optional Fallback Promotion | Select a promotion to display when a user doesn’t qualify for any promotions. If you don’t include a fallback promotion and a user doesn’t qualify for an offer, the default website experience displays. The default global template returns a single offer decision. If your template developer has adjusted the template to return more offer decisions, make sure that the number of fallback options matches the number of promotion decisions.

