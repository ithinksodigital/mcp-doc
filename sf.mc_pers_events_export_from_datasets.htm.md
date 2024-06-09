

# Export Events from a Personalization Dataset

You can export the events in a Personalization dataset to a CSV or JSON file.
Events are the rows that appear in the event stream. Each event can have an
action and several custom fields associated with it. You can use the exported
file to analyze how fields are associated with one another, and to find
statistical trends. You can adjust the time period for the export to get the
specific data you need.

### Required User Permissions

Permissions Needed  
---  
To export a dataset: | A role with Configure Dataset permissions  
  
![3ad6ebb1-f555-43a3-90f1-1b12c9b5a93b]

Note This process is for data sampling on an as-needed basis. If you want to
export large amounts of data regularly, contact your Salesforce representative
for more information about the Personalization Data Warehouse solution.

  1. Click the avatar icon (![78c46da7-cee3-4759-81fd-93a5616e32e7]) in the upper right corner of Personalization.

Alternatively, click the dataset selector.

  2. From the resulting dropdown menu, select **Manage Datasets**.
  3. Click the **Export Events** icon (![e46ee3c1-82f5-4940-bc32-367fc62d536a]) for the desired dataset.
  4. Select the options you want in the Export Events dialog.

Option | Description  
---|---  
**Start** | Start date for the events you want to export.   
**End** | End date for the events you want to export.   
**User Filter** | Filter to export only events associated with specified user or account IDs.   
**Limit** | Number of events you want to export. The default value is 1000 events.   
**Separator** | Separator value used when exporting events in CSV format. The default value is a comma.  
**Quote Char** | Quote character used when exporting events in CSV format. The default is double straight quotes.   
**Fields** | Filter to include only specified fields. If left blank, all fields are exported.   
**Include Formatted Date and Time checkbox** | Include a timestamp next to each event.   
  
  5. Click **OK**.

