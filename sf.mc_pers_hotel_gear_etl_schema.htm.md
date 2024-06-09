

# Booking ETL File Schema

If you send data from your hotel booking system to Personalization, configure
your file according to the Booking ETL file schema.

## File Name Format

`booking-YYYY-MM-DD_HH-MM-SS.csv`

## Required Identity Fields

You must include one identity field in your Booking ETL file. Depending on
whether you use the multiple identities system, the required identity field is
different.

Field Name  | Minimum Requirements  | Sample Values  | Maximum Length  | Data Type   
---|---|---|---|---  
  
  * `userId`
  * another identity attribute, such as email address

| Required.

  * If you aren’t using Personalization's multiple identities system, you must include a user ID for each record. The user ID must be one that the Personalization platform tracks so that it can attach events to the specific user profile.
  * If you’re using Personalization's multiple identities system, you must include at least one identity attribute because ETL file loads don’t reference userID. You can include multiple identity attributes for a single user by adding multiple columns to the file. For more information, see [Guidelines for Sending Multiple Identities in a Booking ETL File](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_etl_multiple_identities.htm&language=en_US&type=5 "If you use the multiple identities system, you must include at least one identity attribute in the Booking ETL file. You can send multiple identity attributes for a single bookingID by adding multiple identity attribute columns in the file."). 

|

  * user168515262
  * jdoe@test.com

| 120 | String  
  
## Other Required Fields

There are additional fields that you must include in any Booking ETL file you
send. Match the field names and meet the requirements.

Field Name  | Minimum Requirements  | Sample Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`bookingId` |  Required. The `bookingId` is a unique identifier for an individual booking, and is a requirement for each record in the file. All line items from a booking must share a `bookingId`. Sort Booking ETL files by bookingID so that all records that share a `bookingId` are in consecutive rows. | 860340254 | 255 | String  
`bookingDate` |  Required. The `bookingDate` is the date of the transaction. Format booking date and time strings in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. Personalization uses the first booking record for a `bookingId` to define the overall order of booking events. Personalization stores all dates in UTC time. | 2020-10-152020-01-09T11:24:59Z | 1023 | Date  
`productId` |  Required. The `productId` represents the product in the catalog that is booked in the transaction. If the ID doesn’t reflect an existing product in the catalog, Personalization creates an item in your catalog with the `productId`. The `productId` value must match the format of other product IDs that exist in your catalog, that you send through the Product ETL data feed, or that you track on your website. | prod001,prod1101 | 255 | String  
`price` |  Required. The `price` is the unit price to charge the user. Use a period as the decimal separator. Don’t include a thousand separator. Personalization multiplies the price by the quantity to determine the total cost of the booking record. For example, if the price is $1.10 and the quantity is 3, the total cost of the line item is $3.30. | 150, 63.25, 10 | 1023 | Decimal  
`quantity` |  Required. The `quantity` is the net quantity a user purchases. Personalization multiplies the quantity by the price to determine the total cost of the line item in the transaction. Personalization adds all line items for a single bookingID, which equals the total value of the order. | 1, 50, 100 | 1023 | Integer  
`attribute:property` |  Required. The property name that is associated with the booking. The property name must match the property catalog object that’s stored with the catalog item being booked in the transaction. | Downtown Main Hotel | 255 | String  
`attribute:bookedCheckInDate` |  Required. Format the scheduled check-in date in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. Multiple line items for the same booking must have the same check-in date. | 2020-10-152020-01-09T11:24:59Z | 1023 | Date  
`attribute: bookedCheckOutDate` |  Required. Format the scheduled check-out date in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. Multiple line items for the same booking must have the same check-out date. | 2020-10-152020-01-09T11:24:59Z | 1023 | Date  
`attribute: adults` |  Required. The number of adults on the booking. | 1, 2 | 1023 | Integer  
  
## System Fields

Additional system fields aren’t required in the file, but if you include them,
you must match the field names and meet the requirements.

Field Name  | Minimum Requirements  | Sample Values  | Maximum Length  | Data Type   
---|---|---|---|---  
`attribute:checkInTime` | 

  * Format the scheduled check-in time in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. 
  * Multiple line items for the same booking must have the same check-in time.
  * If you don’t send a value, the system assigns the required check-in date value until you send a check-in time in a subsequent Booking ETL file. For more information, see [Update a Booking](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_booking_update.htm&language=en_US&type=5 "You can use the Booking ETL data feed to update booking information in Personalization, such as updating a check-in time that wasn’t in the initial booking."). 

| 2020-10-152020-01-09T11:24:59Z | 1023 | Date  
`attribute:checkOutTime` | 

  * Format the scheduled check-out time in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. 
  * Multiple line items for the same booking must have the same check-out time.
  * If you don’t send a value, the system assigns the required check-out date value until you send a check-out time in a subsequent Booking ETL file. For more information, see [Update a Booking](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_booking_update.htm&language=en_US&type=5 "You can use the Booking ETL data feed to update booking information in Personalization, such as updating a check-in time that wasn’t in the initial booking."). 

| 2020-10-152020-01-09T11:24:59Z | 1023 | Date  
`attribute:children` | The number of children on the booking. If you don’t send a value, the system assigns a value of 0. | 2, 3 | 1023 | Integer  
`attribute:bookingStatus` | The current state of the booking, which your administrator must configure for the Hotel Gear. The value in the ETL file and in the Hotel Gear configuration screen aren’t case-sensitive. For more information, see [Activate the Hotel Gear](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_activate.htm&language=en_US&type=5 "Activate the Hotel Gear to bring in data from your hotel booking systems. The Hotel Gear is dataset-specific, so you must activate it for each dataset that has campaigns or promotions that you want to target with booking system data. You send booking system data by the Booking ETL data feed."). | Reserved, Canceled, In-House, No Show | 255 | String  
`attribute:currency` | The currency of the transaction. The currency must be consistent across all records in a transaction. If you don’t send a currency, the system assigns the currency defined in Catalog Setup for that dataset. Currency must be in [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html) format and include three uppercase letters. | USD, AUD, EUR | 3 | String

