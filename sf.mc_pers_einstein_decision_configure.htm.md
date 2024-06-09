

# Configure Einstein Decisions

Einstein Decisions analyzes many unique data points when determining the right
experience to present to a particular user. This data includes user behaviors
as well as contextual data, such as device type, time of day, and demographic
data. Einstein Decisions can also reference segment membership and user
attribute data, along with catalog objects you create in your catalog. To
determine which data Einstein Decisions references, you define the machine
learning features on the Feature Engineering page. Typically, a data science
or analytics team member configures the feature engineering options for
Einstein Decisions.

### Required Editions and User Permissions

Available in: Premium edition  
---  
  
  

Permissions Needed  
---  
To configure Einstein Decisions: | A role with Contextual Bandit Create/Edit permissions  
  
  1. From the **Machine Learning** section of the main navigation, select **Einstein Decisions** | **Feature Engineering**.
  2. Select the training target from the **Bandit Target** dropdown—**Click** , **Conversion** , or **Goal Completion**. 
  3. Select the features you want to use while training the machine learning models.
  4. To include specific user segments, click **+Segment** in the **Segment Membership** section and select options from the dropdown.
  5. To include specific locations, click **+Geography** in the **Geography** section and select options from the dropdown.
  6. To include custom attributes, click **+Attribute** in the **Custom Attribute** section and select options from the dropdown.
  7. To include recent user actions with catalog objects, click **+Catalog Object** in the **Catalog Object Interaction History** section and select options from the dropdown.
  8. Click **Save**.

After configuring the training target and feature engineering options, you can
create campaigns with promotions that use Einstein Decisions.

