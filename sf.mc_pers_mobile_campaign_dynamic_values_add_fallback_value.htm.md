

# Add a Fallback Value for Dynamic Content

If dynamic content doesn’t appear because there’s no correlating value, you
can add a fallback value that shows instead.

### Required Editions and User Permissions

Available in: Premium Edition  
---  
  
  

Permissions Needed  
---  
To create or edit mobile campaigns: | A role with Campaign Create/Edit permissions  
  
  1. [Add dynamic content to your mobile campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_mobile_campaign_dynamic_values.htm&language=en_US&type=5 "You can add dynamic values, such as the mobile app user’s name, location, and email, to all mobile campaign types.").
  2. In the dynamic attribute for which you want to add a fallback value, add a second parameter in the following syntax, changing DEFAULT_TEXT to the text you want to use: `#field(${user.userName}, "DEFAULT_TEXT")`
  3. To create a dynamic message with a custom field, use the following syntax, replacing MY_CUSTOM_FIELD with your custom field name:`${user.attributes.MY_CUSTOM_FIELD}`

It’s important to add "attributes" between "user" and your custom field name
for the message to display properly.

Also, this alternate syntax must be used if MY_CUSTOM_FIELD contains a space:
`${user.attributes.get('MY_CUSTOM_FIELD')}`

![d97d5c46-7e93-4e7f-a73f-25991112d4a0]

Example

The following example uses the word "Visitor" as the second parameter. This
dynamic content is part of a campaign message with the qualified visitor's
userName. If there’s no value for the userName attribute, the message shows
"Visitor" instead.

    
    
    #field(${user.userName}, "Visitor")

