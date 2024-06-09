

# Rule Categories

There are a variety of rules that you can add for campaign targeting and rule-
based campaign experiences when you create or edit a campaign.

## Profile Objects

Profile Object rules show the campaign based on specific user profile objects.

Rule | Shows the Campaign When  
---|---  
Object Aggregation | The user profile object attribute aggregation meets specific criteria.  
Object Match | The user profile object count matches specific criteria.  
  
## Source

Source rules show the campaign based on the user’s technology.

Rule | Shows the Campaign When  
---|---  
Application | The user is or isn’t using a specific app.  
Browser | The user has a specific browser. If you include multiple browsers, Personalization uses OR logic.  
Channel | The user is or isn’t using a specific channel.  
Device | The user has a specific type of device, such as a mobile phone or game console. If you include multiple device types, Personalization uses OR logic.   
ISP | The user has or doesn’t have a specific internet service provider. If you include multiple ISPs, Personalization uses OR logic.   
Operating System | The user has a specific type of operating system. If you include multiple operating systems, Personalization uses OR logic.   
  
## Geography

Geography rules show the campaign based on the physical location of the user.
For example, when you want the campaign to appear to users in a certain
country. If you include multiple locations, Personalization uses OR logic.

Rule | Shows the Campaign When  
---|---  
City | The user is or isn’t in a specific city or town.  
Country | The user is or isn’t in a specific country.  
Location | The user is within a certain distance of a specific latitude/longitude.  
State | The user is or isn’t in a specific US state or region.  
ZIP Code | The user is or isn’t in a specific ZIP code.  
  
## Weather

Weather rules show the campaign based on the weather for a user’s location.

Rule | Shows the Campaign When  
---|---  
Temperature | The temperature at a user's location is at most, at least, or between a specific number of degrees. Personalization uses the user’s local temperature scale.  
Weather Conditions | The weather meets certain conditions, such as rain or snow. If you include multiple conditions, Personalization uses OR logic.  
  
## Visit Behavior

Visit Behavior rules show the campaign based on specific actions of a user.

Rule | Shows the Campaign When  
---|---  
Action | A user completes a specific action. If you include multiple actions, Personalization uses OR logic.  
Page Count | A user views a specific number of pages during a visit.  
Page Type | A user visits pages of a specific type (defined in the site map for your dataset). For example, when a user visits a product detail page.  
URL | The user visits a specific URL.  
Visit Count | A user visits your website a specific number of times.  
Visit Duration | A user visits your website a specific amount of time.  
  
## Referrers

Referrer rules show the campaign based on how the user arrives at your
website. If you include multiple referrer rules, Personalization uses OR
logic.

Rule | Shows the Campaign When  
---|---  
Referrer Domain | An external domain refers the user.  
Referrer Medium | An external medium refers the user.  
Referrer Search Terms | Specific external search terms refer the user. This feature can be limited by the end user's search engine. Google and Bing, for example, don’t pass organic and paid search terms for referral.  
Referrer Source | A specific source, such as a mobile app, refers the user. This rule is available only if you have a mobile app.  
Referrer Subdomain | An external subdomain refers the user.  
Referrer URL | A specific external URL refers the user.  
  
## User Attributes

User Attribute rules show the campaign based on whether the user has specific
user attributes.

## Firmographic

Firmographic rules show the campaign based on the user’s company or industry.

![01067cf3-ea01-412e-bb0b-f3bf4103cf94]

Note These rules are available only if you have B2B Detect.

Rule | Shows the Campaign When  
---|---  
Company Name | The user's company is one of the specified companies. If you include multiple companies, Personalization uses OR logic.  
Industry | The user's industry is one of the specified industries. If you include multiple industries, Personalization uses OR logic.   
  
## Audience

Audience rules show the campaign based on specific segments the user does or
doesn’t belong to. If you include multiple segments, Personalization uses AND
logic.

## Template-Controlled Rules

Certain rules are controlled at the template level, and a developer must
configure them. Examples include the following:

Rule | Shows  
---|---  
Time on Page (Delay) | A message when a user is on the page for a certain amount of time. For example, a user is reading an article about the importance of drinking more water. After 15 seconds of reading, you want a message to appear about ordering home delivery of bottled water.  
Inactivity | A message when a user is inactive on the page for a certain number (or fraction) of seconds or minutes.  
Page scroll | A message when a user scrolls a certain percentage of the page. This behavior is an indicator of engagement and a good time to deliver a particular message.  
Bounce | Experiences to users who are about to leave your page (“second chance” messages). Typical parameters for this rule are 0.05 seconds of delay and inactive space set as 20 px from the top of the page. These parameters capture the behavior of users who are leaving the page.  
  
#### See Also

  * [Campaign Targeting Rules and Rule-based Tests](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_rule_based_test.htm&language=en_US&type=5 "Rules determine when, where, and how your campaigns display and who sees them. You can add rules when you create or edit a campaign at the campaign level for campaign targeting or when defining rule-based test experiences.")
  * [Create a Web Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_create.htm&language=en_US&type=5 "Using a web campaign, you can personalize various aspects of your website for your users based on their behavior, affinities, preferences, location, or other qualifying criteria. You can create web campaigns from templates in your dataset. The templates provide a framework that defines the campaign placement, copy and creative locations, and general campaign design.")

