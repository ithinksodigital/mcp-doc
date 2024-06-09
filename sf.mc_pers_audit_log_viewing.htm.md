

# View the Personalization Audit Log

Administrators can use Marketing Cloud Personalization’s Audit Log to view
access and activity records in support of compliance and investigation
efforts. The Audit Log includes events related to authentication, user
management, API token management, campaigns, templates, catalog
configurations, and other activity for a dataset.

### Required User Permissions

Permissions Needed  
---  
To view the Audit Log: | A role with Administrator permissions  
  
  1. From the bottom section of the main navigation, select **Audits**.

Audit events are grouped by event type, and include the following, as well as
other events:

Item | Description  
---|---  
**API Token** | Events related to API token management. For example, a user creates an API token.  
**Authentication** | Events related to user authentication. For example, a user logs in to Personalization.  
**Campaign** | Events related to campaigns. For example, a user creates a campaign.  
  
  2. To filter by user, affected object ID, account, or action type, click the **Filter By** field and select a filter.
  3. To filter by date to see only those events that happened during a specific time period, change the date selector at the top.
  4. To display a detailed JSON representation of an object affected by an event, select an event and view the **Current** tab.
  5. To compare two events that affect the same object:
    1. Click the **Filter By** field and select **Affected Object ID**.
    2. Select the first event.
    3. Press the SHIFT key and select the second event.
    4. View the difference between the two versions of the affected object.

