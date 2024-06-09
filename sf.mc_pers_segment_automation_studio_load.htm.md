

# Define an Automation for Segment Exports

Configure and schedule an automation for segment exports. You can also text
the automation before activating it.

### Required User Permissions

Permissions Needed  
---  
To define an automation: | A role with Administrator permissions  
  
  1. From the main navigation in Marketing Cloud, select **Journey Builder** | **Automation Studio**. 
  2. Click **New Automation**. 
    1. Drag **Schedule** from the **Starting Sources** section to the **Start with a Starting Source** dotted circle. 
    2. Click **Configure**. 
    3. Enter a **Start Date** and **Time**. 

![029df3f3-083d-4b0e-937b-db18564b2d4f]

Note Be sure not to set a start date and time that occurs before the date you
expect to finish end-to-end testing of this process.

    4. Confirm that the **Time Zone** is correct or change it. 
    5. Select the **Repeat as Daily every 1 day(s)** option. 
    6. Set the **End** as a number of occurrences, a specific date, or never. 
    7. Click **Done**. 
  3. Drag **Import File** onto the workflow canvas. 
    1. Click **Choose** to select an object for that activity. 
    2. Click **Create New Import Definition**. 
    3. Enter a **Name** for the activity that matches the segment so you can identify it in Automation Studio. 
    4. Add a **Description** , if desired, such as details about the Personalization segment rules. 
    5. You can leave **External Key** blank, or add one as necessary. 
    6. To receive a notification after the import completes, select **Send notification email to** and enter the email address. 
    7. Click **Next**. 
  4. Select the **File Location** that you created previously.
  5. Create the **File Naming Pattern** in the format `SegmentExport_[SEGMENT_ID]_%%Year%%-%%Month%%-%%Day%%.csv`, replacing [SEGMENT_ID] with the segment ID for the segment you’re exporting.
  6. As part of end-to-end testing, confirm that the **Example File Name** matches the file dropped in the SFTP inbound folder (such as SegmentExport_[SEGMENT_ID]_2022-04-15.csv). 
  7. Configure the following settings: 

Setting | Description  
---|---  
**Date Format:** | English (United States)   
**Delimiter:** | Comma  
**Respect double quotes (") as a text delimiter:** | Selected  
**Skip rows with bad data:** | Selected  
  
    1. Select any **Advanced File Options** you want. 
    2. Click **Next**.
  8. Locate the data extension you created previously.
  9. Click **Next**.
  10. Select **Add and Update** as the **Data Action**.
  11. Select **Map by Header Row**.

![76b03b36-fbc5-45fd-84e3-c5aa6a9b12f9]

Note Attribute names in the segment you’re exporting must match the field
names in the data extension. If the data extension column names don’t match,
select **Map by Ordinal** or **Map Manually**.

  12. Click **Next**.
  13. Review the configuration.
  14. Click **Finish**.
  15. Add and configure more activities as necessary.
  16. Click **Save**.
  17. To test the automation, click **Run Once**. New records appear on the target data extension.

![157c7841-0fe2-4c4e-bac1-0fa9b5b3d791]

Note To test the automation, there must be a file in the outbound SFTP folder.

  18. When testing is complete, activate the automation by clicking **Active** and then **Activate**.

Previous

**[Find a Segment’s
ID](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_id_find.htm&language=en_US&type=5
"You use a segment’s ID when defining its automation process in Automation
Studio. There are also instances when you need a segment’s ID for an ETL data
feed.")**

