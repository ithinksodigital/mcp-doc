

# Export a Segment to Marketing Cloud

Set up a nightly feed or a one-time export to synchronize Personalization
segments with Marketing Cloud. For example, you can synchronize a segment to
Marketing Cloud to target a specific group with an email communication.

### Required User Permissions

Permissions Needed  
---  
To export a segment: | A role with Segments Create/Edit and Bulk Event Export permissions  
  
  1. Before you can export a segment to Marketing Cloud, set up an SFTP account if you don’t have one. See [Create an SFTP Account](https://help.salesforce.com/s/articleView?id=sf.mc_pers_sftp_account_create.htm&language=en_US&type=5 "Send and receive data from an automated platform safely and securely using ETL Integration. After you create an SFTP account, add the credentials to your FTP client.").

Before you begin, support must enable the Segment File Exporter gear for your
dataset. Your Personalization contract defines the volume of records you can
export. Refer to your contract or contact your account representative for more
information.

The Personalization system exports the segment as a CSV file named
SegmentExport_${segmentId}_YYYY-MM-DD.csv.

  2. From the main navigation, select **User Segments** | **User Segments**.
  3. Double-click the segment you want to export.

![ced5874e-6a72-46cb-9e35-585c6069f9b7]

Note If you’re creating a segment, you must save it before you perform the
following steps.

  4. Click the **Setup** tab.
  5. Select **Sync to Other Systems** | **SegmentFileExporter**.
  6. In the **Segment Sync Setup** dialog that appears:
    1. Select **sfmcContactKey** and **emailAddress** from the **User Attributes** dropdown.

![66e53f52-3324-4ec0-b7be-f8e740dcb69b]

Note The Segment File Exporter automatically includes the User ID and Segment
Membership attributes, and you can select up to 10 additional ones. The order
that you add the user profile attributes determines their column order in the
exported file. If you want to make adjustments, you can add or remove up to 10
attributes after the initial setup.

    2. You can enter a prefix into the **File Prefix** field that identifies the file with a meaningful name. 
    3. To set up a nightly sync of the segment, select **Enable**. 

![87dcc996-797a-421b-9ae5-2c46a6df7559]

Note The sync runs at night in Eastern time (ET), but not at a specific time.

    4. Select **Run Export** | **Run Full Export**.
    5. Click **Save**.
  7. Click **Save** to save any segment changes.

After the initial full export, the nightly job provides Personalization
segment membership changes (delta) since the previous run.

  * Users who have since joined the Personalization segment are added to the corresponding export with a value of `true` in the **segmentmembership** column.
  * Users who have been removed from the Personalization segment are added to the corresponding export with a value of `false` in the **segmentmembership** column.

Next

**[Connect the Personalization SFTP to Marketing Cloud for Segment
Exports](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_sftp_load_marketing_cloud.htm&language=en_US&type=5
"To receive Personalization segments, configure the Personalization SFTP in
Marketing Cloud. You can create a file location and add your existing SFTP
account details.")**

