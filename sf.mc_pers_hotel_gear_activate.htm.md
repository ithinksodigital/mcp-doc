

# Activate the Hotel Gear

Activate the Hotel Gear to bring in data from your hotel booking systems. The
Hotel Gear is dataset-specific, so you must activate it for each dataset that
has campaigns or promotions that you want to target with booking system data.
You send booking system data by the Booking ETL data feed.

### Required User Permissions

Permissions Needed  
---  
To activate the Hotel Gear: | A role with Administrator permissions  
  
  1. Select the dataset.
  2. From the main navigation, select **Gears** | **Gears**.
  3. From the list of gears, select **Hotel**. 
  4. From the dropdown in the right pane, select **Enabled**.
  5. To complete configuration, click **Configure**.
  6. Enter each **Booking Status** you plan to send through the Booking ETL data feed and press **Enter**.

Tip | Description  
---|---  
Booking Status Match | Each booking status must match a booking status in the ETL file you send.  
Case Insensitive | The booking statuses aren’t case-sensitive. For example, if you enter the booking status of “booked”, the status can be “Booked” in the ETL file.  
Segments and Campaign Targeting Rules | After you complete Hotel Gear configuration, the booking statuses you enter are available for Hotel segments and Hotel campaign targeting rules.  
  
  7. To sort booking and booking add-on ETL files by bookingID, select **Hotel Booking ETLSort Before Grouping**. If you don’t select this option, you must sort the ETL files by bookingID before you send it to Personalization.
  8. Save your work.
  9. Proceed to the next steps, which include:

Option | Description  
---|---  
**Feeds Dashboard** | Use the Booking ETL data feed or the Booking Add-On ETL data feed to send data to Personalization.  
**Segments and Campaign Targeting Rules** | Build segments and add campaign targeting rules using Hotel Gear Rules.  
**Catalog** | Use the Booking ETL data feed to add properties and transaction types. Then use the Booking Add-On ETL data feed to create associations between transaction types, such as rooms or room service, and properties. If your product catalog isn’t configured, activate the Hotel Gear. Personalization creates a product catalog and associates it with the property catalog.  
  

#### See Also

  * [Hotel Rules](https://help.salesforce.com/s/articleView?id=sf.mc_pers_hotel_gear_hotel_rule.htm&language=en_US&type=5 "Use hotel rules for web and server-side campaign targeting, or for segmenting customers. You can group or target customers based on traveler details. For example, hotel rules can consider travel party size, booking status, scheduled check-in or check-out time, number of nights’ stay over a time range, or add-ons purchased.")

