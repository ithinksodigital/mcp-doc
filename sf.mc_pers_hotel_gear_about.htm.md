

# About the Hotel Gear

The Hotel Gear is part of the Personalization ETL framework for ETL (extract,
transform, and load data) jobs. The Hotel Gear includes two ETLs (Booking and
Booking Add-Ons) and a set of rules available for segmentation, campaign, and
promotion targeting.

## Booking State Hotel Rule

The booking state is one of the hotel rules you use for segmentation and
campaign targeting. This rule includes things such as booked, completed,
checked-in, canceled, and other guest statuses.

After you activate the Hotel Gear, you must identify the booking states that
you’re sending to Personalization to use for segmentation and targeting. Enter
them as they appear in your booking system because they must match the states
that you send in the ETL file.

## Sorting Records

Records with the same bookingID must be sorted together. You can select the
option in the Hotel Gear configuration so that Personalization sorts the file,
or you can sort the file before you send it to Personalization.

## Ways to Use Hotel Gear

There are many ways to use the Hotel Gear to import data to target your
customers based on previous activity, loyalty status, and specific actions or
behaviors.

Approach | Description  
---|---  
Targeted Offers | Tailor offers to certain groups of customers based on segment membership or a customer’s previous reservation. For example, you can provide offers based on a customer's past booking at a property in New York City.  
Target Experiences Based on a Booking Schedule | Trigger a check-in date mobile push notification that includes personalized messaging and recommended add-ons, such as an early check-in, parking, or other upgrades.  
Loyalty Sign-Ups | Message customers who aren’t loyalty members with the number of points they accrue on an upcoming stay after they sign up for the loyalty program.  
Loyalty Tier | Motivate customers who have stayed a certain number of nights and are close to the next loyalty tier. For example, “You’ve stayed 45 nights this year. Platinum status is 50 nights."  
Add-On Purchases | Suggest upgrades to customers who have an upcoming stay or are currently checked in and haven’t purchased any add-ons.  
Booking Status | Recommend similar properties to customers who have canceled their reservation in the past 30 days.  
Travel Party Size | Target large parties with offers for large group hotel discounts and information about hotel partners in the surrounding area.  
Travel Party (Children on Trip) | Recommend kid-friendly activities in the hotel or surrounding area to customers who have at least one child on their itinerary.  
  
## Initial Order Creation and Updates

When an order is initially created, Personalization includes the information
in Product stats and the Product List page. If the order is subsequently
updated, Personalization includes the update information in the user's order
history and stats (which can be used for targeting using rules).

For example, suppose you run a Booking ETL job to create an order, followed by
an Add-On ETL job that updates the same order. The Booking ETL job represents
the initial creation event that applies to both Product stats and the User
history. The subsequent Add-On ETL job is an update that applies only to the
User history.

