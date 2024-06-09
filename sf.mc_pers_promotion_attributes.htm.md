

# Create a Custom Promotion Attribute

Use custom attributes to determine which promotions appear in a campaign.
Similar to other catalog item types, custom attributes can also be returned as
the output of a decision. When creating a promotion, adding a custom attribute
is optional, but it’s recommended.

### Required User Permissions

Permissions Needed  
---  
To create promotion attributes: | A role with Catalog Create/Edit permissions  
  
After you have configured a custom attribute, you can assign a value to the
attribute when creating or editing a promotion. Supported attribute types
include string, integer, decimal, date, and boolean.

Custom attributes are useful in a promotion as a decision filter or as a
decision output. A template developer can perform exact match filtering for a
promotion attribute to determine which promotions are eligible to return in a
campaign or from an Einstein Decision. For example, if a promotion attribute,
loyaltyTier, has a value of Silver, the template developer can specify to only
return promotions with a loyaltyTier of Silver. After determining which
promotion to return, either with rules or Einstein Decisions, a template
developer can also configure a campaign to return a text-based attribute
value. For example, if you’re using Einstein Decisions to display a call to
action, you can store the text as an attribute on each call-to-action
promotion. Then, you can return the text value for that attribute.

  1. To create a custom attribute, select **Settings** | **Catalog and Profile Objects** | **Promotion** | **New Attribute**. 
  2. Configure the attribute and save it.

#### See Also

  * [Create a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_create.htm&language=en_US&type=5 "Create a campaign promotion to offer special deals and promote specific products. When creating a promotion, the only required information is the name and the URL of the landing page. For a promotion to return in a campaign, you must have an asset associated with the promotion. Adding eligibility criteria, promotion attributes, and related catalog objects is recommended. A promotion attribute determines which promotions appear in a campaign. Personalization uses related catalog objects to track and measure customer affinities across item types in your catalog.")
  * [Einstein Decisions](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_decision.htm&language=en_US&type=5 "When a user views a promotion on your website, Marketing Cloud Personalization captures the user's context—including whether they’re a returning visitor, the device they’re using, and other information that provides insight into that user. Einstein Decisions, Personalization’s machine learning approach for next-best-offer decisioning, uses that context to predict the value of showing a specific offer to a particular user.")

