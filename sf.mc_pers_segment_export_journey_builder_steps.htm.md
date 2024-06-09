

# Steps to Export a Segment to Journey Builder

Complete these steps to export a segment to Journey Builder.

### Required User Permissions

Permissions Needed  
---  
To export a segment: | A role with Segments Create/Edit and Bulk Event Export permissions  
  
Before you can export a segment to Journey Builder, you must perform the
following integration tasks:

  * [Set Up Marketing Cloud and Journey Builder for Segment Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_marketing_cloud_journey_builder.htm&language=en_US&type=5 "To support exporting Personalization segments to Journey Builder, perform setup tasks in Marketing Cloud and Journey Builder.")

  * [Set Up Identity Types for Segment Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_identity_type.htm&language=en_US&type=5 "You must set up the identity types in the Personalization system to support exporting Personalization segments to Journey Builder.")

The Journey Builder segment listener doesn’t support segments that calculate
on a daily basis, such as "Shoppers who didn’t purchase in the last day." The
segment must include an action that users complete for membership. If that
action occurs before the ETL feed populates the attribute, the Personalization
system doesn’t add the segment user to Journey Builder.

For example, consider a segment that includes "attribute: favorite color =
blue" and "did action X today." If the feed runs at 3 AM and populates the
attribute for a user, when the user completes the action later that day, they
join the segment and the Personalization system sends it to Journey Builder.
However, if the feed runs at 7 PM and populates the attribute for a user who
completed the action earlier that day, the user joins the segment, but the
Personalization system doesn’t send it to Journey Builder.

  1. From the main navigation, select **User Segments** | **User Segments**.
  2. Double-click the segment you want to export.

![94bd2b25-d71e-4536-a5b5-c0f1d9e389e6]

Note If you’re creating a segment, you must save it before performing the
following steps.

  3. Click the **Setup** tab.
  4. Select **Sync to Other Systems** | **AddToJourneyBuilderOnJoin**.

The **Segment Sync Setup** dialog that appears.

  5. Select your journey entry source from the **Journey API Event** dropdown.
  6. From the **Marketing Cloud Contact Key** dropdown, select an identifier that contains the appropriate consent information in Marketing Cloud. 

![df84c7ac-969e-4d01-817f-6e131254a935]

Note Typically, the identifier is the Salesforce Marketing Cloud contact key.

  7. From the **Email Address** dropdown, select an identifier.
  8. Select **Enable**. 
  9. Click **Save**.
  10. In **User Segments** , click **Save** to save any segment changes.

![bfb5a1f5-532d-4431-8fb1-8766d30a4586]

Example

You can create a segment of users who view your product more than three times
in a week, then trigger a journey for users that join that segment. Or you can
trigger a journey for users that sign up for a webinar.

Previous

**[Set Up Identity Types for Segment
Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_identity_type.htm&language=en_US&type=5
"You must set up the identity types in the Personalization system to support
exporting Personalization segments to Journey Builder.")**

