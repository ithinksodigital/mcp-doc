

# Use the Salesforce Interactions SDK to Track Booking Transactions

Use the Marketing Cloud Personalization module of the Salesforce Interactions
SDK and configure your sitemap to track a booking transaction by mapping the
order object.

### Required User Permissions

Permissions Needed  
---  
To change the Salesforce Interactions SDK: | A role with Administrator permissions  
  
You can use the order object to track primary booking transactions in the
sitemap by mapping orderID to bookingID. However, you can only update booking
metadata like check-in or check-out date, number of adults, and number of
children, using the Booking ETL.

  1. To update the metadata on a primary booking transaction that the Marketing Cloud Personalization module of the Salesforce Interactions SDK captures, match the bookingID in the Booking ETL to the Salesforce Interactions SDK bookingID. However, you can’t use the sitemap to update a booking that came in by the Booking ETL. 
  2. To associate add-ons with a booking that the Salesforce Interactions SDK captures, the add-ons must have the same bookingID as the Salesforce Interactions SDK booking. If you purchase add-ons separately from the original booking, you can only associate those add-ons to the primary bookingID using the Booking Add-on ETL.

#### See Also

  * [ _Developer Documentation_ : order object](https://developer.salesforce.com/docs/marketing/personalization/guide/event-options-evergage.html#the-order-object)
  * [ _Developer Documentation_ : Marketing Cloud Personalization Web Integration](https://developer.salesforce.com/docs/marketing/personalization/guide/web-integration.html)

