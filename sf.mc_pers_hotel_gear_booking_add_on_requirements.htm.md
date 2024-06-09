

# Booking Add-On ETL Requirements

Learn about requirements for using the Booking Add-On ETL.

You can send booking add-on transactions, such as room service or travel
transportation, to Personalization to improve the details of a customer's
reservation. You can apply multiple booking add-ons to a single booking by
including the same bookingID for all add-on transactions.

Each booking must include a bookingID, which associates details with the
booking. Personalization uses bookingID to update booking information for
multiple records grouped by the same bookingID, such as multiple rooms
associated with the same bookingID. Personalization treats rows with matching
bookingIDs as a single booking transaction. So, the user identifier, booking
date, property, and check-in and check-out dates and times must match for
Personalization to associate records with a single booking. Group the file by
bookingID before you send it or have Personalization sort the file before
loading. If the file isn’t sorted, the data load fails. For more information,
see
[.](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_activate.htm&language=en_US&type=5
"Activate the Hotel Gear to bring in data from your hotel booking systems. The
Hotel Gear is dataset-specific, so you must activate it for each dataset that
has campaigns or promotions that you want to target with booking system data.
You send booking system data by the Booking ETL data feed.")

Include the same bookingID for each add-on transaction. The bookingID connects
each booking add-on to its parent booking transaction. Personalization applies
any booking add-ons to the booking with a matching bookingID. If no matching
bookingID exists in the system when you upload the Booking ETL file,
Personalization creates a parent booking for any add-ons with the bookingID.
The new booking only includes the add-ons you upload. You can update the
booking with the additional information about the stay using the Booking ETL
data feed. For more information, see [Update a
Booking](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_booking_update.htm&language=en_US&type=5
"You can use the Booking ETL data feed to update booking information in
Personalization, such as updating a check-in time that wasn’t in the initial
booking.").

The customer identifier for the booking and any booking add-ons must match. If
the customer identifier doesn’t match, Personalization creates a duplicate
booking for the mismatched identifier. A matching bookingID doesn’t trigger a
merge on user records. For more information, see [Booking Add-On ETL File
Schema](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_booking_add_on_schema.htm&language=en_US&type=5
"If you send booking add-on data from your hotel booking system to
Personalization, configure your file according to the Booking Add-On ETL file
schema.").

If you use the multiple identities system, you must include at least one
identity attribute in the Booking Add-On ETL file. To send in multiple
identity attributes for a single bookingID, add multiple identity attribute
columns in the file. If you don’t use the multiple identities system,
Personalization merges the profiles based on userID. For more information, see
[Guidelines for Sending Multiple Identities in a Booking ETL
File](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_etl_multiple_identities.htm&language=en_US&type=5
"If you use the multiple identities system, you must include at least one
identity attribute in the Booking ETL file. You can send multiple identity
attributes for a single bookingID by adding multiple identity attribute
columns in the file.") and [Booking Add-On ETL File
Schema](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_booking_add_on_schema.htm&language=en_US&type=5
"If you send booking add-on data from your hotel booking system to
Personalization, configure your file according to the Booking Add-On ETL file
schema.").

