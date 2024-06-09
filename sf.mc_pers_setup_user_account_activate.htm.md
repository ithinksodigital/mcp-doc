

# Activate a User Account

Marketing Cloud users must work with an administrator to create a
Personalization user account. Before Marketing Cloud users can use
Personalization, administrators for Marketing Cloud and Personalization must
coordinate with users to set up permissions and access. After a Marketing
Cloud administrator enables Personalization for a user, the user navigates to
Personalization in Marketing Cloud, which creates their Personalization user
account. After the user creates their account, a Personalization administrator
can assign role-based permissions to the account.

### Required User Permissions

Permissions Needed  
---  
To set Personalization permissions: | Marketing Cloud Administrator permissions  
To create and assign roles: | Personalization Administrator permissions  
  
  1. In Marketing Cloud, select **Setup** | **Users** | **Users**.
  2. Select the checkbox for the user that needs access to __ Personalization, and click **Manage Roles**.
  3. On the Setup Users screen, under Permissions, click **Edit Permissions**.
  4. To expand options, click **+** next to Personalization. 
  5. Assign the level of access.
    1. To grant administrator access with full permissions to all datasets, in the Allow column, select **Administrator**. 
    2. To grant user access with varying permissions, in the Allow column, select **Access**. 
  6. Click **Save**.

![75bd82e6-cacf-4702-a08d-313344c2a38c]

Note Users can’t access any dataset in their Personalization account until an
administrator assigns them a role in Personalization. Before an administrator
can assign a user a role, the user must first select Personalization in
Marketing Cloud.

  7. Request that the user select **Personalization** from the Marketing Cloud main navigation.
    1. Personalization creates the user account without any permissions to any datasets in the account.
    2. The user sees the message “You don’t have any permissions for this dataset. Contact your administrator or switch datasets.” 
  8. After the user logs in to Personalization, grant role-based permissions to the user account.
  9. After the user creates an account in Personalization, a Personalization administrator creates and assigns roles to the user account. For more information, see [Add a User Role](https://help.salesforce.com/s/articleView?id=sf.mc_pers_user_role_add.htm&language=en_US&type=5 "Use a default role that you can modify, or create roles with permissions that meet your security requirements and business needs. Because roles are dataset-specific, Personalization users can have different roles in different datasets. Although a role is dataset-specific, when you add a role, it’s available to select in all datasets.").

![93ab898d-3f2a-475f-82c6-102e327b166a]

Example

You can restrict access to certain datasets within an account by user. For
example, you can give some users View Only access to your production dataset
and also grant them full access to create campaigns on your test dataset.

#### See Also

  * [Personalization Permissions in Marketing Cloud Engagement](https://help.salesforce.com/s/articleView?id=sf.mc_pers_setup_marketing_cloud_permissions.htm&language=en_US&type=5 "You can open Personalization directly from Marketing Cloud Engagement after an administrator sets up access.")

