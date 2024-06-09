

# Export a Segment as a CSV File

Export segment data as a CSV file.

### Required User Permissions

Permissions Needed  
---  
To export a segment: | A role with Segments Create/Edit permissions  
  
![c7fd1d30-f88d-47f7-ab29-0a800b664ccf]

Note Exported segment data is accurate to the time it is exported. Because
this data is taken directly from the Personalization database, values can
sometimes differ from data displayed in the Personalization interface.

  1. From the main navigation, select **User Segments** | **User Segments**.
  2. Double-click the segment you want to export.
  3. Click **Export**.
  4. From the dialog that appears, select an option from the**Custom Fields** section:

Option | Description  
---|---  
Include all custom fields | Includes all custom user profile attributes in the exported file.To view the user profile attributes, select **Settings** | **Attributes** from the main navigation.  
Exclude all custom fields | Excludes custom fields from the exported file. The Personalization system includes only built-in user attributes, such as userId and segment rule conditions, as columns in the exported file.  
Include only specific custom fields | Includes only the custom user profile attributes you select from the dropdown that appears. If you select this option and don’t choose additional attributes, the Personalization system excludes all custom attributes in the exported file.  
  
  5. Select an option from the **Built-In User Fields** section:

Option | Description  
---|---  
Include all built in user fields | Includes all built-in fields, such as userId, emailAddress, displayName, firstActivity, lastActivity, engagementScore, and segmentMemberships, in the exported file.  
Exclude all built-in user fields | Excludes all built-in fields except the userId.  
Include only specific built-in fields | Includes only the built-in user fields you select from the dropdown that appears. If you select this option and don’t choose additional fields, the Personalization system includes only the userId (and accountName if your dataset has accounts enabled) in the exported file.  
  
  6. To include segment membership information, select **Include segment membership**. 
    1. Select an option from the **Export Format** section:

Option | Description  
---|---  
Single column named “filtermemberships” | Rows contain segment names denoting user membership.  
Multicolumn | Each column heading corresponds to a segment name, and rows contain “yes” or “no” to denote membership in a segment.  
  
    2. Select an option from the **Filter Options** section:

Option | Description  
---|---  
Include all segments | Includes all other segments that the users in this segment are members of.  
Include only specific segments | Includes only segments that you select from the dropdown that appears.  
  
  7. To exclude anonymous users, select **Exclude anonymous users from export**.
  8. Click **Start Export**.

