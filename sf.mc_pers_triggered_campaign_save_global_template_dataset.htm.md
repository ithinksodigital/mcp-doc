

# Configure a Triggered Campaign Template

A triggered template defines the data to pass to Journey Builder. You can
modify it for each campaign experience, such as which recipe to show to the
qualified user. To create a triggered campaign, you must have a triggered
template in your dataset. Marketing Cloud Personalization includes a standard
template that you can add fields to. If you need options other than what’s
included in the default template, have your developer create a template.

### Required User Permissions

Permissions Needed  
---  
To configure a triggered template: | A role with Templates > Publish/Delete permissions  
  
Your Marketing Cloud Engagement data extension must include a ContactKey
field, which is included by default in the standard triggered template.

  1. From the main navigation, select **Triggered** | **Server-Side and Triggered Templates**.
  2. From the New Template dropdown menu, select **Global Templates**.

The standard triggered template includes default fields that are automatically
added to the Journey Builder journey.

Field | Description  
---|---  
Trigger_Type | A text field that contains the name of the trigger type, which is one of these values:
     * SegmentLeave
     * SegmentJoin
     * EventAction
     * CartAbandonment
     * BrowseAbandonment
     * NewItemInFavoriteCategory
     * ProductBackInStock
     * ProductExpiringSoon
     * ProductLowInventory
     * ProductPriceReduction
To learn more about trigger types, see [User
Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_user.htm&language=en_US&type=5
"A user trigger activates a campaign based on user behavior.") and [Catalog
Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_catalog.htm&language=en_US&type=5
"A catalog trigger activates a campaign based on updates or changes to item
data in your catalog. The trigger activates after a change in your catalog,
but what drives the trigger is the amount of time the user views an item
before the catalog change occurs.").  
Trigger_Segment | A text field that contains the name of the segment that triggered a campaign. Only the Segment Leave and Segment Join trigger types can populate this field.  
Trigger_Action | A text field that contains the name of the action that triggered a campaign. Only the Event Action trigger type can populate this field.  
Trigger_Catalog_Items | A text field that contains a JSON representation of the catalog items related to the trigger, such as a list of abandoned cart products. Because this field contains information in a JSON format, use the maximum available text field size when you add it to the Marketing Cloud Engagement event data extension. The following trigger types can populate this field value:
     * CartAbandonment
     * BrowseAbandonment
     * NewItemInFavoriteCategory
     * ProductBackInStock
     * ProductExpiringSoon
     * ProductLowInventory
     * ProductPriceReduction  
Campaign | A text field that contains the triggered campaign identifier.  
Experience | A text field that contains the triggered campaign experience identifier.  
  
  3. Select any of the following optional settings.

To make the data for these fields available in Journey Builder, create
corresponding fields in the Marketing Cloud Engagement data extension and
configure them as nullable.

Setting | Description  
---|---  
User Attributes | Select user attributes to send to the Journey Builder journey. Field names in the Marketing Cloud Engagement data extension must match the user attribute names.  
Recommendations | A text field that allows you to add a Recommendations block to an email in Marketing Cloud Engagement. This field contains a JSON representation of recommended catalog items based on the recipe you select. To support the JSON format, use the maximum available text field size when you add it to the Engagement event data extension.  
Additional_Recommendations | A second text field that contains a JSON representation of recommended catalog items based on the recipe you select. To support the JSON format, use the maximum available text field size when you add it to the Marketing Cloud Engagement event data extension.  
Segments | A text field that contains a comma-separated list of segments a user is a member of. This list only includes the segments you select in the template for the campaign experience.  
  
  4. Save the template.

