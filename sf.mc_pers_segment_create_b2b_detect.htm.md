

# Create a Segment Based on B2B Detect Data

Create segments for your campaigns that target users according to IP data
sources and NAICS industry codes. This feature is available only with B2B
Detect. Using B2B Detect, you can create personalized calls-to-action, case
studies, and banner images based on a user’s industry or company name. You use
three location rules to create the segment for B2B Detect data.

### Required User Permissions

Permissions Needed  
---  
To create a segment: | A role with Segments Create/Edit permissions  
  
  1. In the **Audiences** section of the main navigation, select **User Segments** | **User Segments**.
  2. Click **New Segment**.
  3. Enter a **Segment Name** that describes its purpose.
  4. Select **Location** from the **Select Category** dropdown. 
    1. Select **Company** from the **Select Location Rule** dropdown.
    2. Select **Contains one of** from the **User’s Company** dropdown.
    3. Begin typing the company name and then select it from the dropdown list that appears.
    4. Add more companies as necessary.
  5. To create the second rule, click **New Rule** and ensure the **And** logical operator is selected.
    1. Select **Location** from the **Select Category** dropdown.
    2. Select **Near** from the **Select Location Rule** dropdown.
    3. Select **ZIP code** from the **User’s** dropdown.
    4. Enter a number into the **is within** | **miles of** field.
    5. Begin typing the ZIP code and then select it from the dropdown list that appears.
  6. To create the third rule, click **New Rule** and ensure the **And** logical operator is selected.
    1. Select **Location** from the **Select Category** dropdown.
    2. Select **Industry** from the **Select Location Rule** dropdown.
    3. Select **Is one of** from the **User’s Industry** dropdown.
    4. Begin typing the industry name and then select it from the dropdown list that appears.
    5. Add more industries as necessary.
  7. Click **Save**. The Personalization system displays the **Users** tab with a list of users that meet the segment’s criteria. 
  8. Click the **Membership** , **Segment Compare** , and **Category Affinities** tabs for data analysis and further targeting.

#### See Also

  * [B2B Detect](https://help.salesforce.com/s/articleView?id=sf.mc_pers_b2b_detect.htm&language=en_US&type=5 "B2B Detect lets you access firmographic data about your users, such as their industry, beginning with their first interaction. The addition of firmographic data allows Marketing Cloud Personalization to provide more targeted personalization to your accounts and their users.")

