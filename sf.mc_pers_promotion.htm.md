

# Campaign Promotions

Offer your customers special deals or advertise specific products with
campaign promotions in Marketing Cloud Personalization. A promotion is an
image that encourages customers to click through for more details. You can
deploy promotion images on a web page or in an email, including call-to-action
messages or incentives to engage customers and achieve specific business
goals. You can also use promotions with Einstein Decisions for rule-based
decisions and machine learning to target customers in multiple channels.

In addition to products and content, you can use the Personalization catalog
to prioritize decisions around the next-best action for each individual
engaging with your company. Before adding promotions to campaigns, consider
creating a comprehensive promotions strategy to improve personalization of
recommendations across channels. The Einstein Decisions model trains with a
variety of different data, including related catalog object data.

  * **[Prerequisites for Promotions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_prerequisites.htm&language=en_US&type=5)**  
To create and use promotions, review and complete these setup steps.

  * **[Create a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_create.htm&language=en_US&type=5)**  
Create a campaign promotion to offer special deals and promote specific
products. When creating a promotion, the only required information is the name
and the URL of the landing page. For a promotion to return in a campaign, you
must have an asset associated with the promotion. Adding eligibility criteria,
promotion attributes, and related catalog objects is recommended. A promotion
attribute determines which promotions appear in a campaign. Personalization
uses related catalog objects to track and measure customer affinities across
item types in your catalog.

  * **[Add Assets to a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_asset_add.htm&language=en_US&type=5)**  
For a promotion to appear in a campaign, it must have an associated asset,
such as an uploaded image or a URL that points to an external image.

  * **[Create a Custom Promotion Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_attributes.htm&language=en_US&type=5)**  
Use custom attributes to determine which promotions appear in a campaign.
Similar to other catalog item types, custom attributes can also be returned as
the output of a decision. When creating a promotion, adding a custom attribute
is optional, but it’s recommended.

  * **[Create a Related Catalog Object for a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_related_catalog_object.htm&language=en_US&type=5)**  
Use related catalog objects to track and measure customer affinities across
item types in your catalog. Related catalog objects provide Einstein Decisions
with data about the promotion to improve the quality of its decisioning.
Related catalog objects are optional in promotions, but they’re recommended
for providing more accurate recommendations.

  * **[Non-Image-Based Promotions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_non_image_based.htm&language=en_US&type=5)**  
Use a non-image-based promotion with Einstein Decisions to return strings of
text as decisions, such as a call-to-action selection. Typically, you use a
non-image-based promotion with a server-side campaign, and the Personalization
response is a string that the client computer uses. The process for creating a
non-image-based promotion is the same as an image-based promotion. Depending
on your template options, you can also define a promotion fallback.

  * **[Promotion and Asset Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_limits.htm&language=en_US&type=5)**  
Marketing Cloud Personalization has limits per dataset for promotions,
segments, and assets.

