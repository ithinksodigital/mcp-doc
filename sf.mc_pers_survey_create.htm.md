

# Create a Survey

Create a survey for a web campaign.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create a survey: | A role with Configure Dataset and Campaign View permissions  
To use the JSON survey editor: | Global Admin permissions  
  
Surveys are deployed in web campaigns, so you have access to all the targeting
rules and testing capabilities in Personalization. You can use survey data to
create user segments, enhance personalization experiences, A/B test to
validate business impact, and analyze feedback results. You can also clone a
survey a survey or build one using the JSON survey editor for developers. For
more information, refer to the [surveyJS
documentation](https://surveyjs.io/form-library/documentation/overview).

![e4f938c7-d9af-4271-b875-0732d71542c8]

Note If you don’t see the Surveys menu in Personalization and your account was
provisioned before April 7, 2021, request a Gears refresh for your account
from support. If you’re unsure whether a Gears refresh has already occurred
for your account, ask your account admin who can see the Gears list on your
account.

  1. From the main navigation, select **Surveys.**
  2. Click **+New Survey.**
  3. Enter a survey name.
  4. To enter a survey title, click **Setup** and enter a survey **Title**.

![c00b073c-0155-40e1-8a2f-d5b3b4b399cf]

Note The survey title only appears to respondents if you select **Show/hide
title** and**** a developer enables an element for it in a web campaign
template.

  5. To change the**Question title location** from the **top** , select **Setup** and in the **Question** section, select **bottom** or **left** of the question.
  6. To change the default question title format, in **Setup** in the **Question** section, enter a **Question title template**. The default format shows the question number followed by the required symbol followed by the question title.
  7. If you want your survey to have multiple pages, click **+Page** to add as many pages as you want. 

![3378e639-2a70-44bb-acac-07b80cd211a7]

Note You can’t drag questions directly between pages, but you can save a
question to the Toolbox to reuse it by clicking the diskette icon.

  8. To show page titles on each page of the survey, click **Setup** and select **Show page titles**. 
  9. To change the page title, in the Survey Designer, click the default page name (page 1), click the pencil icon to open the **Edit** window, make changes, and click **Apply**.
  10. To show page numbers, in **Setup** and select **Show page numbers**.
  11. Add survey questions.
    1. In the **Toolbox** , drag the question type to the survey canvas. Each new question appears after the previous question.
    2. Enter question and answer text.
    3. To rearrange the questions, drag a question to a different location.
    4. To place multiple questions next to each other, click the pencil icon and deselect **Start on new line.**
    5. To change the numbering (or lettering) system for questions, select **Setup** and in the **Question** section, enter numbers or letters in the **question start index**. If you don’t enter a value, questions begin with “1.”
    6. To hide question numbers, in **Setup** in the **Question** section, select **Off** from the **Show question numbers** dropdown.
    7. To allow the survey respondent to immediately begin typing an answer without selecting the answer field, in **Setup** in the **Question** section, select **Focus first question on changing the page**.
    8. Save your work.
  12. To edit questions and answers:
    1. To edit an individual question or answer, click the pencil icon next to the item. When done, click the check icon to close the editor.
    2. To add another answer, select the question and click +.
    3. To change the order of the answer options or questions, click the pencil icon and in the Answers section, use the hamburger icon to reorder the answer options.
  13. To save changes, click **Save** to stay in the survey or **Save and Close** to close the survey.
  14. To make the survey available for visitors to complete, work with a developer to add it to a web campaign using the survey gear.

