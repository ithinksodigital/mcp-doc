

# Configure Integration with Journey Builder

Set up the integration between Journey Builder and Marketing Cloud
Personalization.

### Required User Permissions

Permissions Needed  
---  
To integrate with Journey Builder: | A role with Administrator permissions  
  
Before you can begin integration setup, refer to [Prerequisites for Journey
Builder
Integration](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_marketing_cloud_journey_builder_prereqs.htm&language=en_US&type=5
"Meet these prerequisites before configuring Journey Builder integration.").

These steps describe how to add a Personalization Journey Builder Activity to
an existing Journey Builder journey.

  1. In Journey Builder, select the journey you want to use.
  2. In the **Customer Updates** section, drag **Salesforce Personalization Activity** onto the canvas.
  3. Click the **Salesforce Personalization Activity** on the canvas.
  4. In the **Interaction Studio Activity Summary** pane, click **Configure**.
  5. On the **Dataset** tab, select the dataset for the site, brand, or other item you want to send data to.
  6. On the **Action Name** tab, select **Static** or **Dynamic** from the **Type** dropdown list.

Item | Description  
---|---  
**Static** | When selected, each person on the journey records the same action. For example, everyone on this journey is on the Welcome journey.  
**Dynamic** | When selected, each person on the journey records an action specified by an attribute in Marketing Cloud Engagement. For example, one person is on a Welcome Credit Card journey and another is on a Welcome Mortgage journey.  
  
  7. For **Static** types, enter an **Action Name** to record in Personalization.
  8. For **Dynamic** types, select a value from **Journey Data** or **Contact Data**.

**Journey Data** is a snapshot of the data in the source data extension when
the visitor enters the journey. This option appears only after you’ve
configured an entry source. Data can change after a visitor enters the
journey. To use the most current data, select from **Contact Data**.

  9. On the **Identifiers** tab, select a **Salesforce Personalization Identifier** , and then map a **Marketing Cloud Attribute** to that identifier.

For example, you can map the contact ID in Marketing Cloud Engagement to
customerId in Personalization. The Personalization identity system combines
records in Personalization that have the same value.

![98254370-e572-4fc5-8483-b7d4307048ad]

Important To avoid having merged records that don’t represent the same
individual, make sure that Salesforce Personalization Identifiers and any
Marketing Cloud Engagement attributes that you select have unique values.

  10. (Optional) Add additional identifiers, making sure to map the desired Marketing Cloud Engagement attribute.
  11. (Optional) On the **Attributes** tab, click **Add Attribute** to add any Personalization attributes you want to use for targeting, segmentation, and personalization.
  12. To view a summary of the activity configuration, click **Summary**.
  13. Click **Done** to save the activity.

