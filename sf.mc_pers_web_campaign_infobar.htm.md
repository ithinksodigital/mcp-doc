

# Infobar Web Campaigns

Infobars appear at the top or bottom of a web page, and are designed to
capture a user’s attention. Infobars typically have limited real estate and
are most often used to communicate important temporary information, such as a
special announcement or a one-day discount.

## Use Infobars in Web Campaigns

For infobars, A/B test campaigns are great opportunities to test out different
copy or calls-to-action to see what drives the most click-throughs or sign-
ups. With rule-based campaigns, you can target different types of users to
encourage them to take certain actions. For example, you can target an infobar
web campaign to new users encouraging them to sign up for your loyalty program
or newsletter. For users who are already registered, you can encourage them to
download your app or explore a new piece of content or collection of products.

Infobars typically target a global content zone, so they appear on all pages
of your website. If you want your infobar to appear only on certain pages,
include page targeting logic at the campaign level to restrict where it
appears.

You can create infobar web campaigns using one of the built-in global
templates, or using a custom template that a developer creates.

## Infobar Web Templates

The infobar web templates available to you can differ in name and
configuration options due to modifications by your developer. If you need
additional styling or configuration options, ask your template developer about
modifying the template.

Both infobar global templates include a call-to-action. If you want to create
an infobar web campaign without a call-to-action, work with your template
developer to remove it from the template.

**Infobar with Call-to-Action** —Select this template to display an infobar
with a single call-to-action message.

Item | Description  
---|---  
**Style** | This template offers the options of **Dark on Light** (dark text on a light image) and **Light on Dark** (light text on a dark image) for flexibility according to the background image.  
**Message Text** | This text appears as the call-to-action message in the infobar.  
**CTA Text** | This text appears on the prestyled call-to-action button within the infobar.  
**CTA Destination URL** | This URL is the page where users land when they click the call-to-action button.  
  
![5289ba47-603b-454b-aac3-db3779e83a4f]

Note If the landing page doesn't align with your targeting logic or campaign
goals, you can create a confusing experience for your users.

**Infobar with User Attribute and Call-to-Action** —Select this template to
display an infobar with a message that references a user profile attribute, in
addition to a call-to-action message.

Item | Description  
---|---  
**Style** | This template offers the options of **Dark on Light** (dark text on a light image) and **Light on Dark** (light text on a dark image) for flexibility according to the background image.  
**Pre-Attribute Message Text** | This text appears in the message before the user profile attribute. For example, when using the firstName attribute of the Unified Customer Profile for a message of "Hi Bob!", you enter "Hi" in this field.  
**User Attribute Default** | If the user profile attribute isn’t available, this text displays to prevent a blank space from appearing in the message. For example, for a message of "Hi Bob!", you can enter "there" in this field so the message displays as "Hi there!" if the user profile attribute isn’t available. To ensure a positive experience, either define a default value for the user profile attribute or target the campaign only to users that have an association with the attribute. For example, for the firstName attribute, define a value that displays if the user's name isn’t available or target the campaign only to users with a stored first name value. If you want to reference a different user profile attribute, ask your template developer to update the template accordingly.  
**Post-Attribute Message Text** | This text appears in the message after the user profile attribute. For example, for a message of "Hi Bob!", you enter "!" in this field. This field is optional.  
**CTA Text** | This text appears on the prestyled call-to-action button within the infobar.  
**CTA Destination URL** | This URL is the page where users land when they click the call-to-action button.  
  
![b0baf32f-7e6d-4e76-a010-e45278f843f7]

Note If the landing page doesn't align with your targeting logic or campaign
goals, you can create a confusing experience for your users.

#### See Also

  * [Create a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_create.htm&language=en_US&type=5 "Using a web campaign, you can personalize various aspects of your website for your users based on their behavior, affinities, preferences, location, or other qualifying criteria. You can create web campaigns from templates in your dataset. The templates provide a framework that defines the campaign placement, copy and creative locations, and general campaign design.")
  * [ _Video_ : Create A/B Test and Control Groups](https://www.youtube.com/watch?v=-hKk5LufJ0E)
  * [ _Video_ : Create Rule-Based Campaigns](https://www.youtube.com/watch?v=7frznbLswhk)

