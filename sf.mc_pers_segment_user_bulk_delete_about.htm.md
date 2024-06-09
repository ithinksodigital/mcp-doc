

# Considerations and Consequences for Bulk Deleting Profiles

Before you bulk delete profiles, be sure to review these considerations and
consequences.

## Before You Proceed with Bulk Profile Deletion

  * Before you proceed, determine whether any of your campaigns are actively using the segment for campaign targeting. During a bulk delete job, the segment is disabled. If a campaign references a segment being used in a deletion job, the number of people eligible to receive the campaign decreases, as users are deleted which will likely contribute to a drop in impressions on that campaign. 
  * Bulk deletion permanently removes users from the Personalization system but not from the data warehouse. For GDPR and CCPA deletion requests, use the User Look-Up and Deletion API. For more information, see the developer documentation at [User Lookup & Deletion API](https://developer.salesforce.com/docs/marketing/personalization/guide/user-look-up-deletion-api.html?q=user%20delete).
  * Bulk deleted users cannot be recovered.
  * When a large bulk deletion job completes, you might observe some shifts in various platform reporting metrics.
  * You can run only one bulk deletion by segment job at a time. For example, you cannot have two bulk deletion jobs running concurrently for different segments. 

## Commonly Asked Questions

Question | Answer  
---|---  
How long will my job take? | Depending on the size of a segment (based on user count), jobs can run from just a few minutes to up to five days. Jobs typically progress at a deletion speed of about 100 users per second. Use this factor to calculate a rough estimate on how long a job will take to complete, and whether multiple jobs might be required for an exceptionally large segment.  
The job has completed, but I still see some users in the segment list. What does this mean? | Personalization cannot guarantee that a single bulk deletion job will remove all users in the segment. If users remain after the job completes, you need to run one or more subsequent bulk deletion jobs to eliminate the rest.  
The job has completed and the user list is blank, but the user tab still shows a number next to it. Are all the users actually deleted? | The value shown in the user tab is a cached value. If no users show in the list below, then no users exist in the segment. To refresh the user tab, log out and log in to Marketing Cloud.

