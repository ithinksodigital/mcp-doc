

# Web Campaign Template Properties

A web campaign template provides a structure for delivering personalized
experiences and activation campaigns to your website users. Your
Personalization account includes a set of built-in global templates to get you
started creating web campaigns. Each template is a starting framework that
your developer can modify to create custom templates that support your
organization’s needs.

## Content Zones

A content zone is an area on your website that a developer configures to make
it available for personalization in a web campaign or a web campaign
experience. Examples of content zones include a homepage hero, a popup, and an
infobar. A web campaign template includes content zones that you use to
display text, images, buttons, URL links, and input fields. For example, with
the Exit Intent with Email Capture template, a developer must create the
attribute for the email address captured in the web campaign field. The
instructions are included in the template for reference. Each template
includes comprehensive documentation to guide your developer when making
modifications. For more information, see [Content
Zones](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_content_zone.htm&language=en_US&type=5
"A content zone is an area on your website configured to be available for
personalization in a web campaign. A developer defines content zones in the
sitemap for your site. You use content zones to display text, images, buttons,
and input fields. Examples of content zones include a homepage hero, a popup,
and an infobar.").

## Standard Configuration for Global Templates

The following table provides an overview of the standard configuration for
each global template. The templates available to you can have different name
and configuration options if they’ve been changed by your developer.

**Name** |  **Sample Use Cases** |  **Sample Customization Options**  
---|---|---  
Banner with call-to-action | 

  * Homepage hero banner personalization based on affinity segments
  * Landing page lifecycle targeting with a dynamic call-to-action based on lifecycle state
  * Loyalty program registration for nonmembers
  * Third-party data to target prospects

|

  * Number of call-to-action messages
  * Text and call-to-action locations
  * Banner size
  * Banner style, either flat or layered

  
chatbot | 

  * Trigger the chatbot to appear when a person spends more than 1 minute on an application page
  * Trigger the chatbot to appear when someone scrolls down 50% of an FAQ page
  * Suppress the chatbot from appearing for customers with an open support case

|

  * Who should qualify to see the chatbot (campaign/experience targeting rules)
  * When the chatbot should appear based on factors including time on page, inactivity, and scroll depth
  * Integrates with the [Salesforce embedded chatbot (default)](https://developer.salesforce.com/docs/atlas.en-us.250.0.snapins_web_dev.meta/snapins_web_dev/snapins_web_overview.htm), but it can be configured to work with a different chatbot in a similar manner

  
Einstein content recommendations | 

  * Display trending content recommendations on the homepage to engage first-time users.
  * Offer next-best content recommendations to entice deeper engagement on blog and article pages.

|

  * Number of recommended content items
  * Style of recommendations
  * Location of recommendations based on mapped content zones

  
Einstein Decisions | Machine learning-driven next-best-offer decisioning | Number of returned promotions  
Einstein product recommendations | 

  * Display trending product recommendations on the homepage to engage first-time users.
  * Facilitate additional product discovery through co-browse recommendations on product detail pages, and increase cart size with co-buy recommendations on the cart page.

|

  * Number of recommended product items
  * Style of recommendations
  * Location of recommendations based on mapped content zones

  
Exit intent | Recognize classic exit intent behavior (mousing toward the top of the page), and recapture customer interest with a call-to-action, offer, or discount. | 

  * Number of call-to-action messages
  * Text and call-to-action locations
  * Popup image style, either flat or layered
  * Popup contents, such as recipe inclusion

  
Exit intent with email capture | 

  * Turn anonymous users into known customers and extend the number of communication channels for them by strategically timing when to ask for their email.
  * Progressively profile customers by asking for different attributes based on information already known about the customer. For example, ask for a phone number if the emailAddress attribute exists on the profile.

|

  * Text and call-to-action locations
  * Popup image style, either flat or layered
  * Attributes collected

  
Google Analytics segment push | Pass audience segments to Google Analytics. | Limited default options due to the specificity of the template  
Infobar with call-to-action | 

  * Display major announcements, such as COVID-19 updates to global audiences.
  * Add sale or promotion announcements, such as free shipping thresholds or seasonal sales.
  * Announce upcoming events or a webinar registration with a registration link.

|

  * Number of call-to-action messages
  * Infobar styling

  
Infobar with user attribute and call-to-action | 

  * Display an infobar with a user’s name and a call-to-action message.
  * Display an infobar with a user's company name and a call-to-action message.

|

  * Number of call-to-action messages
  * User attribute (user’s name is the default)
  * Text and background colors and styles

  
Manual promotion selector | Use rule-based promotion targeting. | Number of promotions that return  
Redirect | Redirect users to another page.If the page that provides the redirect has campaigns that the user qualifies for, impression stats can be registered for these campaigns, despite the redirect. | —  
Slide-in with call-to-action | 

  * Target customers and prospects with an attention-grabbing slide-in message that includes a call-to-action.
  * Select from a variety of trigger options that determine when the message appears, including time on page, scroll depth, and inactivity.

|

  * Number of call-to-action messages
  * Slide-in location and speed
  * Text and background colors and styles

  
  
#### See Also

  * [Content Zones](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_content_zone.htm&language=en_US&type=5 "A content zone is an area on your website configured to be available for personalization in a web campaign. A developer defines content zones in the sitemap for your site. You use content zones to display text, images, buttons, and input fields. Examples of content zones include a homepage hero, a popup, and an infobar.")

