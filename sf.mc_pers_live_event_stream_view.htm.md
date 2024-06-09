

# View the Live Event Stream

Personalization captures user activity as events. The live event stream
includes events for all of your website visitors.

### Required User Permissions

Permissions Needed  
---  
To view the event stream: | All roles  
To export event data: | Roles with “Audiences > Raw Event Data” permissions  
  
  1. From the main navigation, select **Reports** | **Event Stream**.
  2. To search for a specific visitor’s events, enter the UserID in the **keyword** field.
  3. To narrow events by event type, select the **Event Type** from the dropdown.
  4. To see more information about the event, select an event to open the **Event Detail** pane. The pane includes this standardized data along with any custom attributes captured during the event:

Attribute | Description  
---|---  
**Timestamp** | The day and time when the event happened  
**User ID** | The visitor’s known or anonymous Personalization ID  
**Action** | The event that happened, such as Viewed Item  
**URL** | The page URL involved in the event  
**Client IP** | The visitor’s IP address  
**User Agent** | The technology that captured the event, such as a web browser  
**Beacon Version** | The version of the Personalization JavaScript Beacon (Marketing Cloud Personalization module of the Salesforce Interactions SDK) installed on the website  
**contentZones** | The content zones present in the web event. A content zone is defined as an area on your site that a developer configured in the sitemap to make it eligible for personalization.  
**pageType** | The defined page type captured in the site map for the page involved in the event  
**Channel** | The channel where the event occurred, such as mobile, email, or web  
**ItemAction** | If the event is an interaction, ItemAction shows the interaction defined for the event.  
**Item** | If the event is an interaction, Item shows the items involved in the event.  
**Campaign Stats** | If the event involves a Personalization campaign, Campaign Stats shows the campaign statistic tracked by Personalization.  
  
  5. The event stream refreshes every 15 seconds.
  6. Some stream events are identified by an icon, including impressions, clicks, dismissals, and errors.

