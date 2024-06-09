

# Catalog Triggers

A catalog trigger activates a campaign based on updates or changes to item
data in your catalog. The trigger activates after a change in your catalog,
but what drives the trigger is the amount of time the user views an item
before the catalog change occurs.

  * **[New Item in High-Engagement Category Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_high_engagement_category_new_item.htm&language=en_US&type=5)**  
Reach users when you add a catalog item in a category that they’ve expressed
high interest in. This trigger checks for new items in the user’s high-
engagement categories every 6 hours and activates if the user hasn’t viewed
any of the items for the specified minimum view time. A high-engagement
category is based on behavior criteria that you set, such as view time and a
minimum number of items purchased.

  * **[Product Back in Stock Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_product_back_in_stock.htm&language=en_US&type=5)**  
Use this trigger to reach customers when an out-of-stock product that they
viewed becomes available. The user must have viewed the product while it was
out of stock for a minimum amount of time within a specified number of days.
The trigger checks for products that are back in stock every hour.

  * **[Product Expiring Soon Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_product_expiring_soon.htm&language=en_US&type=5)**  
Use this trigger to reach customers when a product that they spent time
viewing but didn’t purchase will no longer be available. The user must have
viewed the product for a minimum amount of time within a specified number of
days. Marketing Cloud Personalization uses the minimum view time to filter out
customers that look at a product only for 1 second before they navigate away.
Before activating the trigger, Personalization checks that the user didn’t
purchase the product and that the product has at least 5 minutes until
expiration.

  * **[Product Price Reduction Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_product_price_reduction.htm&language=en_US&type=5)**  
Use this trigger to reach customers when a product they viewed but didn’t
purchase drops in price. The user must have viewed the in-stock product for a
minimum amount of time within a specified number of days. Marketing Cloud
Personalization uses a minimum view time to filter out customers that look at
a product only for 1 second before they navigate away. The trigger checks
every 30 minutes for qualifying products that have a price drop greater than
the configured minimum price percent reduction.

  * **[Product Low Inventory Trigger](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_product_low_inventory.htm&language=en_US&type=5)**  
Use this trigger to reach customers when a product they spent time viewing but
didn’t purchase has a low inventory. The user must have viewed the product for
a minimum amount of time within a specified number of days. Marketing Cloud
Personalization uses the minimum view time to filter out customers that look
at a product only for 1 second before they navigate away. The trigger checks
every hour for qualifying products that have an inventory count below the
configured threshold.

