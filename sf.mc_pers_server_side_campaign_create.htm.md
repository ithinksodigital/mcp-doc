

# Create a Server-Side Campaign

You can create server-side campaigns to personalize experiences across
multiple channels with a single campaign.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create a server-side campaign: | A role with Campaigns > Create/Edit permissions  
To publish a server-side campaign: | A role with Campaigns > Publish/Delete permissions  
  
  1. A developer must create a server-side template. For more information, see the developer documentation for [Server-Side Templates](https://developer.salesforce.com/docs/marketing/personalization/guide/server-side-campaigns-templates.html).
  2. From the main navigation, select **Server-Side** | **Server-Side Campaigns**.
  3. Click **New Campaign**.
  4. Name your campaign.
  5. The default campaign targeting rule is channel: Server. If you remove the default channel rule, the campaign requires an authenticated request by the /authevent endpoint with channel set to Server in the call.
    1. To add more campaign targeting rules, in **Campaign Targeting** , click **>**.
    2. Click **Add Rule**.
    3. Select a rule category and subcategory.
    4. Complete other options.
    5. Click **Add Rule** to add more rules for the same campaign. Rules are treated using AND logic.
  6. Configure experiences.
    1. To add an experience, click the **+** next to **EXPERIENCES**. A new experience opens.
    2. Click **Add Template** next to the experience you want to modify.
    3. Select a published template.
    4. Complete template inputs for the experience.
    5. If you configure **Campaign Type** before you add experiences, update the campaign type configuration.
  7. To create an A/B test campaign:
    1. Next to CAMPAIGN TARGETING, click **>**.
    2. Select **A/B TEST**.
    3. (Optional) To change an experience name, double-click it and type in a new name. Because campaign statistics lists each experience name, we recommend that you name experiences based on any unique features of the experience.
    4. Modify the user percentage for each experience and the control group. Users must qualify for an experience to be included in the control group. Users in the control group don’t see the campaign.
  8. To create a rule-based campaign:
    1. Next to CAMPAIGN TARGETING, click **>**.
    2. (Optional) To change an experience name, double-click it and type in a new name. Because campaign statistics lists each experience name, we recommend that you name experiences based on any unique features of the experience.
    3. To include a control group, set the percentage of qualified users in the **Control** field. Users must qualify for an experience to be included in the control group. Users in the control group don’t see the campaign.
    4. To add a rule, click the**+** next to **Add Rule** for the experience you want to modify.
    5. Click **\+ ADD RULE**.
    6. Select a rule category and subcategory.
    7. Complete the other options for the rule.
    8. To add additional rules for the same experience, click **\+ ADD RULE**. Multiple rules in the same experience follow AND logic, so visitors must satisfy all rules, regardless of the order, to qualify for the experience. If a user qualifies for multiple experiences, the user sees the experience highest in the list. To reorder experiences, drag them to the correct order.
  9. **Save** your work.
  10. Have a developer help you test your campaign. For more information, see the developer documentation for [Test Experiences](https://developer.salesforce.com/docs/marketing/personalization/guide/server-side-campaigns-templates.html?q=server-side%20campaigns#test-experiences).

![f1953dbb-2494-493a-8b69-23bb0c52ad18]

Example

  * **Restrict campaign responses.** You can set a campaign targeting rule to restrict campaign responses to certain applications so only customers using the applications see the campaign. You can add a **Source** | **Application** campaign targeting rule, and include only the applications that can send campaign responses, such as mobile or POS. For the campaign to return a response, an inbound request must include one of the applications you configured in the rule.
  * **Build application-specific experiences**. You can set an experience-level application rule to target users on different applications with a relevant experience. Add a **Source** | **Application** experience-level rule, and include only the applications that can send campaign responses, such as mobile or POS. The application must be included in the inbound call for the campaign to return the experience for that application.

