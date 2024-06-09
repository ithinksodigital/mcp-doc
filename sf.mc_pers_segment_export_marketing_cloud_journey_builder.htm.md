

# Set Up Marketing Cloud and Journey Builder for Segment Exports

To support exporting Personalization segments to Journey Builder, perform
setup tasks in Marketing Cloud and Journey Builder.

### Required User Permissions

Permissions Needed  
---  
To set up Marketing Cloud: | A role with Administrator permissions  
To set up Journey Builder: | A role with Administrator permissions  
  
  1. Log in to Marketing Cloud.
  2. Select **Audience Builder** | **Contact Builder** from the menu bar.
  3. Create a sendable data extension. For more information, see [Create a Data Extension in Contact Builder](https://help.salesforce.com/s/articleView?id=sf.mc_cab_create_a_new_data_extension.htm&language=en_US&type=5).
  4. Configure the **ContactKey field:**
    1. Select **Text** as the data type.
    2. If you’re going to set the journey to No Re-entry, select **Primary Key**. If you’re going to set the journey to Re-entry anytime or Re-entry only after exiting, select **Require**.
  5. Specify an **EmailAddress** :
    1. Select **Email Address** as the data type.
    2. Select **Not Required**.
  6. Define the **SegmentName** :
    1. Select **Text** as the data type.
    2. Select **Not required**.
  7. Map SubscriberKey to ContactKey.
  8. Open Journey Builder.
  9. Create a Journey Builder event definition and map it to the data extension you created in Marketing Cloud.
  10. Create a journey with an API entry source using the event definition. For more information, see [Admit Contacts Via API](https://help.salesforce.com/s/articleView?id=sf.mc_jb_admit_contacts_via_api.htm&language=en_US&type=5).
  11. Add additional activities to the journey. For more information, see [Message Activities](https://help.salesforce.com/s/articleView?id=sf.mc_jb_message_activities.htm&language=en_US&type=5).
  12. Save, validate, and publish the journey.

#### See Also

  * [Set Up Identity Types for Segment Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_identity_type.htm&language=en_US&type=5 "You must set up the identity types in the Personalization system to support exporting Personalization segments to Journey Builder.")

Next

**[Set Up Identity Types for Segment
Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_identity_type.htm&language=en_US&type=5
"You must set up the identity types in the Personalization system to support
exporting Personalization segments to Journey Builder.")**

