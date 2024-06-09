

# Create a Promotion

Create a campaign promotion to offer special deals and promote specific
products. When creating a promotion, the only required information is the name
and the URL of the landing page. For a promotion to return in a campaign, you
must have an asset associated with the promotion. Adding eligibility criteria,
promotion attributes, and related catalog objects is recommended. A promotion
attribute determines which promotions appear in a campaign. Personalization
uses related catalog objects to track and measure customer affinities across
item types in your catalog.

### Required User Permissions

Permissions Needed  
---  
To create a promotion: | A role with Catalog Create/Edit permissions  
  
You can also use the Promotion ETL to bring promotions into Personalization.
See [Promotion ETL Data
Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_promotion_data_feed.htm&language=en_US&type=5
"Use the Promotion ETL data feed to add promotions for your catalog for both
rule-based and machine learning-driven cross-channel decisioning.").

  1. In the Catalog section of the main navigation, click **Promotions**.

If you don’t see Promotions listed, confirm that it’s enabled. Select **Settings** | **Catalog and Profile Objects** | **Promotion**. Turn on **Enabled** , and click **Save**.

  2. Click **New Promotion**.
  3. Enter a name for the promotion, the URL of the landing page, and an optional description.
  4. To run the promotion for a specific period, enter the start and end dates. 

If you don’t enter any dates, the promotion is always active and is eligible
to return in a campaign. If you enter only a start date, the promotion remains
active from that date. If you enter only an end date, the promotion starts as
soon as you save it and becomes inactive on the end date.

  5. To set a start time and end time for the promotion, click the clock icons.

The time shown reflects your browser’s local time zone. Personalization stores
all times in UTC time.

  6. To target specific customers based on existing user attributes, in the Eligibility section, click **New Attribute** and add user attributes to the promotion. 

Values entered are case-sensitive. You can switch the Matches toggle to Does
Not Match.

  7. To exclude and include customers from specific segments, select segments from the Include and Exclude dropdown menus.

If you include multiple segments, a customer must be a member of all segments
to qualify for the promotion. If you exclude multiple segments, a customer is
disqualified from the promotion if they’re a member of only one of the
excluded segments. If a customer qualifies for both an included and excluded
segment, Personalization prioritizes the excluded segment, and the customer
doesn’t receive the promotion.

  8. In the Attributes section, select custom attributes to determine which promotions appear in a campaign. You can also create custom attributes after you save the promotion.
  9. If there are existing related catalog objects, you can select them in the Related Catalog Objects section. You can also create related catalog objects after you save the promotion. 
  10. (Optional) For metadata reporting, in the Objective section, select **Item** and **Goal**.
  11. Save your promotion.

For a promotion to appear in a campaign, it must have an associated asset.
Before applying a promotion to a campaign, add the appropriate assets.

#### See Also

  * [Add Assets to a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_asset_add.htm&language=en_US&type=5 "For a promotion to appear in a campaign, it must have an associated asset, such as an uploaded image or a URL that points to an external image.")
  * [Create a Custom Promotion Attribute](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_attributes.htm&language=en_US&type=5 "Use custom attributes to determine which promotions appear in a campaign. Similar to other catalog item types, custom attributes can also be returned as the output of a decision. When creating a promotion, adding a custom attribute is optional, but it’s recommended.")
  * [Create a Related Catalog Object for a Promotion](https://help.salesforce.com/s/articleView?id=sf.mc_pers_promotion_related_catalog_object.htm&language=en_US&type=5 "Use related catalog objects to track and measure customer affinities across item types in your catalog. Related catalog objects provide Einstein Decisions with data about the promotion to improve the quality of its decisioning. Related catalog objects are optional in promotions, but they’re recommended for providing more accurate recommendations.")

