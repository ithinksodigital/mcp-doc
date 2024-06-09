

# Export Events

Export events (that is, user activities) and bring this data into other
systems for further evaluation.

### Required User Permissions

Permissions Needed  
---  
To view the event stream: | All roles  
To export event data: | Roles with “Audiences > Raw Event Data” permissions  
  
  1. From the dataset selector above the main navigation, select **Manage Datasets**.
  2. Click the export icon for the dataset with the events that you want to export.
  3. On the **Export Events** window, configure parameters for the export:

Item | Description  
---|---  
**Start** | Enter the start and end date for the time period of the events export.  
**User Filter** | Restrict events to specific user and account IDs using the sample format: 
     * userId=name@example.com
     * company=Cumulus   
**Limit** | The maximum number of exported rows. The default setting is 1000.  
**Format** | Select the format as CSV, JSON, or JSON Array.  
**Separator** | Choose the value separator. The default is comma-separated.  
**Quote Char** | Enter a CSV quote character to enclose all fields with the specified character.  
**Fields** | Enter field names if you want to include only those fields in the export. If you leave this parameter blank, the export includes all fields.  
**Include Formatted Date and Time** | Select whether to include the formatted date and time in addition to the epoch timestamp. If you don’t select this option, the export includes only the epoch timestamp.  
  
  4. To start the export, click **OK**. When complete, the exported file appears in **Downloads**.

