

# Export a Segment to the Personalization SFTP

Set up a nightly feed or a one-time export to synchronize segments with the
Personalization SFTP. You can then use these segments in other systems to
target cross-channel communications. For example, you can synchronize a
segment to Marketing Cloud to target a specific group with an email
communication.

### Required User Permissions

Permissions Needed  
---  
To export a segment: | A role with administrator permissions  
  
Before exporting a segment to Marketing Cloud, make sure to do the following:

  * Ensure the Segment File Exporter gear is enabled for your dataset. To locate the Segment File Exporter gear, select **Gears** | **Gears** from main navigation to open the Installed Gears page.
  * If you don’t have one, set up an SFTP user. See [Create an SFTP Account](https://help.salesforce.com/s/articleView?id=sf.mc_pers_sftp_account_create.htm&language=en_US&type=5 "Send and receive data from an automated platform safely and securely using ETL Integration. After you create an SFTP account, add the credentials to your FTP client.") for more information.

Your Personalization contract defines the volume of records you can export.
Refer to your contract or contact your account representative for more
information.

  1. From the main navigation, select **User Segments** | **User Segments**.
  2. Double-click the segment you want to export.

![54b47034-e60f-4dc6-ae4e-f9a12fff4c89]

Note If you’re creating a segment, you must save it before you perform the
following steps.

  3. Click the **Setup** tab.
  4. Select **Sync to Other Systems** | **SegmentFileExporter**.
  5. In the **Segment Sync Setup** dialog that appears:
    1. Select the user profile attributes you want to export from the **User Attributes** dropdown.

![be86b144-788e-4a6d-8014-124ff5b54de4]

Note The Personalization system automatically includes the User ID and Segment
Membership attributes, and you can select up to 10 additional ones. The order
that you add the user profile attributes determines their column order in the
exported file. If you want to make adjustments, you can add or remove up to 10
attributes after the initial setup.

    2. You can enter a prefix into the **File Prefix** field that identifies the file with a meaningful name. 
    3. To set up a nightly sync of the segment, select **Enable**. 

![f20b9896-a07e-47cf-8595-632b450d55c5]

Note The sync runs at night in Eastern time (ET), but not at a specific time.

    4. To immediately start a one-time export to SFTP, select **Run Export** | **Run Full Export**.
    5. Click **Save**.
  6. Click **Save** to save any segment changes.

The Personalization system exports the segment as a CSV file named
SegmentExport_${segmentId}_YYYY-MM-DD.csv.

After the initial full export, the nightly job provides Personalization
segment membership changes (delta) since the previous run.

  * Users who have since joined the Personalization segment are added to the corresponding export with a value of `true` in the **segmentmembership** column.
  * Users who have been removed from the Personalization segment are added to the corresponding export with a value of `false` in the **segmentmembership** column.

