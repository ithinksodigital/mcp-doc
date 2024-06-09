

# Guidelines for Sending Multiple Identities in a Booking ETL File

If you use the multiple identities system, you must include at least one
identity attribute in the Booking ETL file. You can send multiple identity
attributes for a single bookingID by adding multiple identity attribute
columns in the file.

## Guidelines

  * To send in multiple identity attributes for a single bookingID, add multiple identity attribute columns in the file using the header format attribute:value. 

  * If you use the multiple identities system, Personalization doesn’t reference the userID attribute in ETL processing. 

  * If you don’t use the multiple identities system, you can send the userID attribute for profile merging.

## Examples

Examples of out-of-the box identity attributes with proper header formatting
include:

  * attribute:emailAddress
  * attribute:sfmcContactKey
  * attribute:customerId
  * attribute:sfcrmContactId
  * attribute:sfcrmLeadId

