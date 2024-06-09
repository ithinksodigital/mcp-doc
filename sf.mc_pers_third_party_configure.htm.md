

# Configure a Third-Party Integration

By integrating with third-party products, you can synchronize user information
that you collect and store in other applications to deliver real-time
personalized experiences across channels. Specifically, this type of
integration focuses on tracking incoming clicks from external, or third party,
campaigns but not impressions.

### Required User Permissions

Permissions Needed  
---  
To configure a third-party integration: | A role with Administrator permissions  
  
  1. From the **Channels & Campaigns** section of the main navigation, select **Third-Party > Integration Setup**.
  2. Select the application with which you want to integrate.

![77ae2089-5ec3-4fdf-9f6b-9d8bd05b5d55]

Note Applications that have a green checkmark are already integrated. If the
application you want to integrate with isn’t listed, click **Add Custom
Product** and add it.

  3. In the **Campaign Match Configuration** section, click the dropdown and select the parameter type: **Landing Page URL** , **Landing Page URL Query Parameter** , **Referrer URL** , or **Referrer URL Query Parameter**.
    1. For Landing Page URL and Referrer URL, select **equals** , **contains** , **exists** , or **matches regex** , and then enter the URL (either a partial, full, or regular expression).
    2. For Landing Page URL Query Parameter and Referrer URL Query Parameter, enter the parameter name (the default is utm_source) and configure the additional fields. 
  4. Edit and delete parameter mappings as needed to meet your integration needs. A list of default parameter mappings is provided. 
  5. To add a parameter mapping, click **Add Parameter Mapping**.
    1. From the dropdown, select a query parameter type and enter a name for it in the following field.
    2. From the next dropdown, select a Personalization target type and enter the target field name that it maps to. 
    3. Click **OK**.
  6. Add other parameter mappings as necessary.
  7. Save your work.

