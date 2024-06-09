

# Set Up Automated Data Sharing Between Personalization and Salesforce CRM

After you configure automated data sharing, Marketing Cloud Personalization
and Salesforce CRM share data on a nightly basis.

### Required User Permissions

Permissions Needed  
---  
To set up data sharing: | A role with Administrator permissions  
  
Decide which data you want to share between Salesforce CRM and
Personalization. For more information, see [Plan Data Sharing Between
Personalization and Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_data_synchronization.htm&language=en_US&type=5
"Before initializing data sharing, decide what data you want to exchange
between Salesforce CRM and Personalization and how you want to match data for
merging. After initialization, Marketing Cloud Personalization shares data
with Salesforce CRM on a nightly basis. Contacts and accounts are shared
automatically, but leads sharing is optional.").

  1. Log in to Personalization as an administrator.

For more information, see [Log In To Personalization from Marketing
Cloud](https://help.salesforce.com/s/articleView?id=sf.mc_pers_login.htm&language=en_US&type=5
"Access Marketing Cloud Personalization from Marketing Cloud Engagement.").

  2. In Personalization, select **Third Party > Integration Setup **from the **Channels & Campaigns** section of the main navigation. 
  3. Select **Salesforce CRM**.
  4. Configure data sharing from Personalization to Salesforce CRM. Click the **Push** tab.
  5. To synchronize more than one Personalization dataset to Salesforce CRM, select **Push data to dataset-specific Salesforce fields** and then enter a text value in the **Dataset-specific field infix** text box. This text is added to the field name as: Interaction Studio_infix_LastActivity.
  6. Select **Create Salesforce field sets to group Interaction Studio fields** if you want to group all Personalization fields in a single field set on your Contact or Account pages.
  7. On the **User** tab, select the data items you want to send to Salesforce CRM.
  8. Click the **Account** tab and select the data items you want to send.
  9. Click **Save**.
  10. Configure data sharing from Salesforce CRM to Personalization. Click the **Pull** tab.
  11. In the **Synchronize Salesforce** section, select the types of Salesforce CRM records you want to synchronize with Personalization—**Contacts** , **Accounts** , and **Leads**. A tab appears for each record type you select.
  12. For each record type, configure the following:
    1. In the **Only pull records** section, you can restrict sharing to include records created or modified after a certain number of days. 

Selecting these options reduces the sync time and allows for incremental
syncs. For example, you can initially pull all leads modified in the past 180
days, and then change the configuration to only pull leads modified in the
past two days. Then the nightly sync only pulls leads modified after the
previous nightly sync. The **Last Created** and **Last Modified** filters are
joined with AND logic, so they’re cumulative.

    2. For specific records, click **+Pull New Salesforce Contact Field**.
    3. From the **Salesforce Field** dropdown, select a field to pull data from.
    4. From the **Evergage User Field** dropdown, select a Personalization field to receive the data. 
    5. To set the field as a unique identifier match between Salesforce CRM and Personalization, select **Match On Field**.
    6. Click **Add** to add the new field.
    7. Add any other fields as necessary.
  13. Click **Save** to save your changes.
  14. Click the **Setup** tab.
  15. To test your setup, click **Synchronize Now**.

Run an on-demand job with **Synchronize Now** to verify your initial
integration setup or confirm setup changes. After your setup is confirmed,
it’s best to rely on automated data sharing instead, which occurs nightly. The
**Synchronize Now** option is available if needed.

  16. When the data sharing is complete, the **Last Synchronized** date and time update, and the status changes to **Success**.

The Salesforce CRM data that you shared is immediately available in
Personalization in reports, filters, and the [Unified Customer
Profile](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_customer_profile.htm&language=en_US&type=5
"The Unified Customer Profile provides a comprehensive view of each of your
users—visitors, customers, prospects, and subscribers—based on their
interactions with your various channels.").

To view Personalization data in Salesforce CRM, you must configure the
applicable record layouts in Salesforce CRM. For more information, see [Show
Personalization Data in Salesforce
CRM](https://help.salesforce.com/s/articleView?id=sf.mc_pers_salesforce_crm_view.htm&language=en_US&type=5
"In Salesforce CRM, display data that was shared by Marketing Cloud
Personalization. For shared contacts, accounts, and leads, configure the
applicable record layout in Salesforce CRM.").

