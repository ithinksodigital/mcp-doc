

# Booking Add-On ETL File Schema

If you send booking add-on data from your hotel booking system to
Personalization, configure your file according to the Booking Add-On ETL file
schema.

## File Name Format

`booking-addon-YYYY-MM-DD_HH-MM-SS.csv`

## Required Identity Fields

You must include one identity field in your Booking ETL file. Depending on
whether you use the multiple identities system, the required identity field is
different.

Field Name  | Minimum Requirements  | Sample Values  | Maximum Length  | Personalization Data Type   
---|---|---|---|---  
  
  * `userId`
  * another identity attribute, such as email address

|  Required.

  * If you aren’t using Personalization's multiple identities system, you must include a user ID for each record. The user ID must be one that the Personalization platform tracks so that it can attach events to the specific user profile.
  * If you’re using Personalization's multiple identities system, you must include at least one identity attribute because ETL file loads don’t reference userID. You can include multiple identity attributes for a single user by adding multiple columns to the file. For more information, see [Guidelines for Sending Multiple Identities in a Booking ETL File](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_etl_multiple_identities.htm&language=en_US&type=5 "If you use the multiple identities system, you must include at least one identity attribute in the Booking ETL file. You can send multiple identity attributes for a single bookingID by adding multiple identity attribute columns in the file.").

|

  * user168515262
  * jdoe@test.com

| 120 | String  
  
## Other Required Fields

There are additional fields that you must include in any Booking ETL file you
send. Match the field names and meet the requirements.

Field Name  | Minimum Requirements  | Sample Values  | Maximum Length  | Personalization Data Type   
---|---|---|---|---  
`bookingId` |  Required. The `bookingId` is a unique identifier for an individual booking and is a requirement for each record in the file. All line items from a booking must share a bookingID. Sort Booking Add-On ETL files by bookingID so that all records that share a bookingID are in consecutive rows. | 860340254 | 255 | String  
`bookingDate` |  Required. The `bookingDate` is the date of the transaction. Format booking date and time strings in the [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. Personalization stores all dates in UTC time. | 2020-10-152020-01-09T11:24:59Z | 1023 | Date  
`productId` |  Required. The `productId` represents the product in the catalog that is purchased as an add-on to a booking. If the ID doesn’t reflect an existing product in the catalog, Personalization creates an item in your catalog with the `productId`. The `productId` value must match the format of other product IDs that exist in your catalog, that you send through a Product ETL data feed, or that you track on your website. | prod001,prod1101 | 255 | String  
`price` |  Required. The `price` is the unit price for the add-on. Use a period as the decimal separator. Don’t include a thousand separator. Personalization multiplies the price by the quantity to determine the total cost of the booking record. For example, if the price is $1.10 and the quantity is 3, the total cost of the line item is $3.30. | 150, 63.25, 10 | 1023 | Decimal  
`quantity` |  Required. The `quantity` is the net quantity a user purchases. Personalization multiplies the quantity by the price to determine the total cost of the line item in the transaction. Personalization adds all line items for a single bookingID, which equals the total value of the order.  | 1, 50, 100 | 1023 | Integer  
  
## System Fields

Additional system fields aren’t required in the file, but if you include them,
you must match the field names and meet the requirements.

Field Name  | Minimum Requirements  | Sample Values  | Maximum Length  | Personalization Data Type   
---|---|---|---|---  
`attribute: currency` | The currency of the transaction. The currency must be consistent across all records in a transaction. If you don’t send a currency, the system assigns the currency defined in Catalog Setup for that dataset. Currency must be in [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) format and include three uppercase letters. | USD, AUD, EUR | 3 | String

