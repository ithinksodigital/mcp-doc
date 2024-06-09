

# Booking ETL File Requirements

Learn about requirements for using the Booking ETL data feed.

There are several requirements for each Booking ETL file you send to
Personalization. For more information, see [Booking ETL File
Schema](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_etl_schema.htm&language=en_US&type=5
"If you send data from your hotel booking system to Personalization, configure
your file according to the Booking ETL file schema.").

  * Each booking must include a bookingID, which associates details with the booking. Personalization uses bookingID to update booking information for multiple records grouped by the same bookingID, such as multiple rooms associated with the same bookingID. Personalization treats rows with matching bookingIDs as a single booking transaction. So, the user identifier, booking date, property, and check-in and check-out dates and times must match for records associated with a single booking. Group the file by bookingID before you send it or have Personalization sort the file before loading. If the file isn’t sorted, the data load fails. For more information, see [Activate the Hotel Gear](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_activate.htm&language=en_US&type=5 "Activate the Hotel Gear to bring in data from your hotel booking systems. The Hotel Gear is dataset-specific, so you must activate it for each dataset that has campaigns or promotions that you want to target with booking system data. You send booking system data by the Booking ETL data feed."). 

  * Include a productId, price, and quantity for each transaction record. In Booking ETL files, you can also include booking details, such as check-in or check-out date and time, property, and party size. However, you must use the Booking Add-On ETL data feed to associate additional add-on line-items with a bookingID. For more information, see [Booking Add-On ETL Requirements](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_booking_add_on_requirements.htm&language=en_US&type=5 "Learn about requirements for using the Booking Add-On ETL."). 

  * Personalization doesn’t merge multiple records with the same bookingID. All records with the same bookingID must have the same user identifier and purchaseDate values. Booking IDs should be unique to a single profile.

  * Configure booking status options on the Hotel Gear configuration screen. The booking status is the current state of a booking, such as canceled, confirmed, or reserved. For the booking status Hotel Rule to reference these values, your administrator must navigate to the configuration screen of the Hotel Gear and enter the corresponding states. 

  * Booking ETL update files must include the bookingStatus attribute and all associated fields. When you update a booking status using the Booking ETL data feed, you must include the updated bookingStatus attribute associated with each booking. The Booking ETL file must include all fields in the booking even if the only value that’s changing is the bookingStatus.

  * If you use the multiple identities system, you must include at least one identity attribute in the Booking ETL file. To send in multiple identity attributes for a single bookingID, add multiple identity attribute columns in the file. If you don’t use the multiple identities system, Personalization merges the profiles based on userID. For more information, see [Guidelines for Sending Multiple Identities in a Booking ETL File](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_etl_multiple_identities.htm&language=en_US&type=5 "If you use the multiple identities system, you must include at least one identity attribute in the Booking ETL file. You can send multiple identity attributes for a single bookingID by adding multiple identity attribute columns in the file.") and [Booking ETL File Schema](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_etl_schema.htm&language=en_US&type=5 "If you send data from your hotel booking system to Personalization, configure your file according to the Booking ETL file schema.").

