

# User Profile Object Rules

Use built-in user profile object rules to help improve cross-channel
personalization in segmentation and web campaign targeting. User profile
objects have two built-in rules—object aggregation and object match.

Rule | Description | Examples  
---|---|---  
Object aggregation | Analyze integer and decimal attributes for user profile objects of the same type.For example, if you have a user profile object called “lease” with an attribute of mileage, and a user profile has multiple leases, you can use the object aggregation rule to apply logic for the mileage attribute for the multiple lease objects.You can use this rule only for user profile objects that have an integer or decimal attribute.  | Example 1—Lease mileage maximum is less than 50,000 for user profile objects matching no specific conditionsExample 2—Lease mileage average is from 25,000 to 50,000 for user profile objects with a status of activeExample 3—Mortgage interest rate average is less than 0.08 for user profile objects matching no specific conditions  
Object match | Find user profiles with user profile objects that meet a certain set of criteria.For example, if you have a user profile object called “lease,” you can find all the users that have at least one lease that satisfies a set of conditions. | Example 1—Lease count is at least 1, and satisfies all of the following conditions:

  * Lease end is in the next 90 days
  * Lease mileage is over 50,000
  * Year is 2022
  * Model is sport edition

Example 2—Mortgage count is at least 1, and satisfies all of the following
conditions:

  * Type is fixed-rate
  * Duration is greater than 10
  * Status is active

Example 3—Support case count is greater than 2, and satisfies any of the
following conditions:

  * Status is open
  * Priority is high

  
  
#### See Also

  * [About User Profile Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_about.htm&language=en_US&type=5 "Learn more about user profile objects.")
  * [Create a User Profile Object](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_profile_object_create.htm&language=en_US&type=5 "Create user profile objects and their relationships to better define your Personalization users. Once created, you can use these objects in segmentation and campaign targeting to improve cross-channel personalization. You update, add, and remove user profile object data profile with the User Profile Object ETL.")

