

# Create a Segment Based on a Specific Action Count

Create segments for your campaigns to target users who complete one or more
actions a specific number of times. To capture users who complete an action a
specific number of times, create two action rules that relate to each other.

### Required User Permissions

Permissions Needed  
---  
To create a segment: | A role with Segments Create/Edit permissions  
  
  1. In the **Audiences** section of the main navigation, select **User Segments** | **User Segments**.
  2. Click **New Segment**.
  3. Enter a **Segment Name** that describes its purpose.
  4. To create the first rule, select **Actions** from the **Select Category** dropdown. 
  5. Select **Action Count** from the **Select Actions Rule** dropdown.
  6. Select **did** from the **User** dropdown.
  7. Select **any of specific actions**.
  8. Begin typing in the **Search Actions** field and select the action from the dropdown that appears.

![5948d590-d4c4-4349-bd25-1af00a65aa99]

Note Actions vary by dataset. You can view the actions for your dataset by selecting **Reports** | **Actions**.

  9. Enter the desired number in the **times** field.
  10. Select **for all time**.
  11. To create the second rule, click **New Rule** and ensure the **And** logical operator is selected.
  12. Select **Actions** from the **Select Category** dropdown. 
  13. Select **Action Count** from the **Select Actions Rule** dropdown.
  14. Select **did not** from the **User** dropdown.
  15. Select **any of specific actions**.
  16. Begin typing in the **Search Actions** field and select the action you selected for the first rule.
  17. In the **times** field, enter a number that is one greater than the number you entered for the first rule.
  18. Select **for all time**.
  19. Click **Save**.

![8927eaf9-d79f-4f0c-ac56-b684a05bb4aa]

Example

To create a segment of users who complete the action "Home" twice, create two
rules. The first rule captures all users who perform the action "Home" two or
more times. The second rule captures all users who don’t perform the action
"Home" three or more times. The second rule acts as a ceiling on the number of
times a user completes the action. Because a user must meet both rules to be
in this segment, the segment contains all users who complete the action "Home"
just two times.

Rule 1 | Rule 2  
---|---  
  
  * Actions
  * Action Count
  * Did
  * Any of the specific actions
  * Home
  * 2
  * For all time

|

  * Actions
  * Action Count
  * Did not
  * Any of the specific actions
  * Home
  * 3
  * For all time

