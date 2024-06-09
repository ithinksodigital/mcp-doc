

# Create a Manual Segment

Create manual segments to group known users, or accounts, based on data that
the Personalization system doesn’t collect or data that’s available through
third-party integrations.

### Required User Permissions

Permissions Needed  
---  
To create a segment: | A role with Segments Create/Edit permissions  
  
  1. In the **Audiences** section of the main navigation, select **User Segments** | **User Segments**.

![7f8e19dc-014c-4cda-9ac4-ac754ce0df36]

Note If your organization markets to businesses, as well as consumers, you can create a manual segment that consists of a fixed, specified list of accounts by selecting **Account Segments** | **Account Segments**.

  2. Select **New Segment** | **Manual Segment**.
  3. Enter a **Segment Name** that describes its purpose.
  4. Click **Save**. The **Users** tab opens so that you can add users to the segment. There are three options for adding users to the segment:
    1. To add users one at a time, enter a user’s name or ID in the **Add User** field on the **Users** tab and select a user from the list that appears.
    2. To add a group of users from a CSV file, click **Upload CSV** on the **Users** tab and select the file.

![73fa3168-429c-402e-8d1d-7fc755fc7927]

Note The CSV file must contain a column with the header value “ID” or “name”
with values that match Personalization system user or account IDs. The file
can include additional columns, and the Personalization system ignores them.

    3. Set up a Manual Segment ETL feed. For more information, see [Manual Segment ETL Data Feed](https://help.salesforce.com/s/articleView?id=sf.mc_pers_etl_manual_segment_data_feed.htm&language=en_US&type=5 "Use the Manual Segment ETL data feeds to maintain manual segments.").

![b65411c1-bf47-47c8-b02e-6d1ff50b61e9]

[](https://help.salesforce.com/s?language=en_US)Example **ID** |  **Name**  
---|---  
betty@example.com | Betty Smith  
john@example.com | John Doe  
tom@example.com | Tom Smith

