

# User Profile Merge Logic

How Personalization merges two or more user profiles depends on whether or not
those profiles share identity types.

When Merging Occurs | When Merging Doesn’t Occur  
---|---  
​​When Personalization merges two or more user profiles, it stores all
historic events, transactions, and interactions for those user profiles based
on the following logic:

  * If an identity type exists for only one user profile, Personalization retains that identity type and adds it to the merged user profile.
  * If an identity type exists in more than one user profile, Personalization retains the identity type with the latest timestamp and adds it to the merged user profile. 
  * If metadata doesn’t exist or doesn't have a timestamp, Personalization uses the system updated timestamp instead.

| If there isn't shared identity type data between the user profiles,
Personalization doesn’t forcefully merge them. For example, Personalization
doesn’t perform a request to rename, or merge, LoyaltyID 123 to LoyaltyID 567
if there's no shared identity type data between the two user profiles.Even
when there’s a matching identity attribute, Personalization doesn’t merge
profiles under these conditions.

  * When attempting to merge an anonymous user to a known user profile, but that known user profile currently has an active session.
  * When attempting to merge anonymous user B with known user X, but anonymous user A already merged with known user X in the last 30 minutes.

