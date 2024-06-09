

# Non-Image-Based Promotions

Use a non-image-based promotion with Einstein Decisions to return strings of
text as decisions, such as a call-to-action selection. Typically, you use a
non-image-based promotion with a server-side campaign, and the Personalization
response is a string that the client computer uses. The process for creating a
non-image-based promotion is the same as an image-based promotion. Depending
on your template options, you can also define a promotion fallback.

A non-image-based promotion requires an asset because a content zone or tag is
necessary for bandit decisioning. The asset can be a placeholder image URL or
a 1x1 pixel image file. Personalization uses the asset’s content zones and
tags to train the bandit and filter which promotions the bandit considers.

Because the asset is just a placeholder for content zone and tag
configuration, promotion attributes help determine the data that
Personalization returns in an Einstein decision. Key factors to consider
include:

  * Attributes that contain information, such as call-to-action text, asset ID, or an action name, can return in the campaign response payload instead of the asset image URL.

  * The campaign response object is configurable in the template. A template developer can determine which information to return for a promotion.

There are several things a template developer must do when configuring a
template for a non-image-based promotion.

  * Use the Einstein Decisions global template as the template baseline.

  * Hard code the eligible content zones or tags, such as Homepage Hero CTA or Add to Cart CTA, into the template server-side code. For more information, see [Einstein Decisions - Server-Side Template](https://developer.salesforce.com/docs/marketing/personalization/guide/einstein-decisions-server-side-template.html).

  * Configure the campaign response object to return the applicable promotion attributes. For example, for a Homepage Hero CTA template, configure the campaign response object to return the Homepage Hero CTA attribute in the promotion.

#### See Also

  * [Create a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_create.htm&language=en_US&type=5 "Create a campaign promotion to offer special deals and promote specific products. When creating a promotion, the only required information is the name and the URL of the landing page. For a promotion to return in a campaign, you must have an asset associated with the promotion. Adding eligibility criteria, promotion attributes, and related catalog objects is recommended. A promotion attribute determines which promotions appear in a campaign. Personalization uses related catalog objects to track and measure customer affinities across item types in your catalog.")
  * [Einstein Decisions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_decision.htm&language=en_US&type=5 "When a user views a promotion on your website, Marketing Cloud Personalization captures the user's context—including whether they’re a returning visitor, the device they’re using, and other information that provides insight into that user. Einstein Decisions, Personalization’s machine learning approach for next-best-offer decisioning, uses that context to predict the value of showing a specific offer to a particular user.")
  * [Server-Side Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_server_side_campaign.htm&language=en_US&type=5 "Server-side campaigns integrate testing and personalization at the server-to-server level. While Marketing Cloud Personalization handles the campaign logic, you need a developer to write the code to call the appropriate APIs and provide information about the website visitor.")

