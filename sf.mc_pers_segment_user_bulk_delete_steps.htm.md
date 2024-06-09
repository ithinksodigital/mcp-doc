

# Steps to Bulk Delete Profiles

Complete these steps to permanently delete profiles that are members of a
Personalization segment. Once deleted, the user data cannot be recovered.

### Required User Permissions

Permissions Needed  
---  
To bulk delete users: | A role with Administrator permissions  
  
![d5af92a1-e41d-46a3-89a1-f4f5bd647dc6]

Important Don’t use this method to process user deletions relating to the
California Consumer Privacy Act (CCPA) or the European Union's General Data
Protection Regulation (GDPR). The Personalization system provides a dedicated
API specifically for deleting users for CCPA, GDPR, and other right-to-be-
forgotten regulations. For more information, see the developer documentation
at [User Lookup & Deletion
API](https://developer.salesforce.com/docs/marketing/personalization/guide/user-
look-up-deletion-api.html?q=user%20delete).

When deleting profiles, keep these considerations in mind.

  * Personalization disables the segment so that additional users don’t join it while the deletion job is in progress.
  * Personalization shows job status notifications on the segment detail screen for the segment associated with this job. 
  * Only one bulk user deletion job can run at a time per dataset.
  * Depending on the size of the segment, the deletion process could take anywhere from a few minutes to up to five days.

Before you proceed, review [Considerations and Consequences for Bulk Deleting
Profiles](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_user_bulk_delete_about.htm&language=en_US&type=5
"Before you bulk delete profiles, be sure to review these considerations and
consequences."). Ensure that you fully understand and accept the implications
of performing this task.

  1. In the **Audiences** section of the main navigation, select **User Segments** | **User Segments**.
  2. Double-click the desired segment.

You can select a segment, a subscriber list, or a manual segment.

  3. Click **Delete All Users in Segment**. 

![75840d2e-8490-414b-ab22-a4f51c745962]

Note If you do not see this button, you are not logged in with sufficient
permissions to perform this task.

  4. Personalization prompts you to confirm that you want to proceed. Read the confirmation message. If you accept the consequences of deleting the users, click the checkbox to indicate your consent.

![de9bb28b-14c3-4c52-9d9e-43cd567817ea]

Warning You can’t stop the bulk deletion process after it starts.

  5. To permanently delete all users in the selected segment, click **Confirm Delete**.
  6. To view the in-progress status of the bulk deletion job, select **User Segments** | **User Segments** , select the **Show Disabled** checkbox, and double-click the segment.

Selecting the checkbox ensures you can see the segment that was disabled at
the beginning of the deletion process. Disabled segments show up in a lighter
weight font.

  7. After performing a bulk deletion, the segment remains disabled. To re-enable it, follow the instructions in [Enable a Disabled Segment](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_enable.htm&language=en_US&type=5 "Re-enable a segment that has been disabled. For example, a segment can be disabled following a bulk deletion of profiles associated with the segment.").

