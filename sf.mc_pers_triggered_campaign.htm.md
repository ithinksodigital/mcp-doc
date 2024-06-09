

# Triggered Campaigns

A trigger is a specific event, such as a visitor behavior or environmental
change that prompts a Marketing Cloud Personalization action, such as sending
an email. You can create a triggered campaign to target different user
segments, provide different experiences for different users, include A/B
testing, or define a campaign schedule or frequency.

You can use a triggered campaign in a variety of ways. For example, send a
promotion to a shopper who has spent time viewing a product but hasn’t
completed a purchase. Remind a new user to complete onboarding steps. Drive
urgency to purchase a product that is on sale. Or, alert a customer that their
favorite item is back in stock.

  * **[Requirements for Creating Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_prerequisites.htm&language=en_US&type=5)**  
To create a triggered campaign, you must configure components in Contact
Builder, Journey Builder, and Personalization.

  * **[Configure a Triggered Campaign Template](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_save_global_template_dataset.htm&language=en_US&type=5)**  
A triggered template defines the data to pass to Journey Builder. You can
modify it for each campaign experience, such as which recipe to show to the
qualified user. To create a triggered campaign, you must have a triggered
template in your dataset. Marketing Cloud Personalization includes a standard
template that you can add fields to. If you need options other than what’s
included in the default template, have your developer create a template.

  * **[Create a Triggered Campaign](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_create.htm&language=en_US&type=5)**  
Use a triggered campaign to launch a journey when a specific action or event
occurs. For example, send a promotion to a shopper who spent time viewing a
product but didn’t purchase. You can recommend unread articles or products to
a visitor who has spent more than 5 minutes reading about a topic. You can
remind new users to complete onboarding steps, or alert sales reps when target
prospects spend a certain amount of time on your site. When creating a
triggered campaign, you can define when to trigger the campaign, which users
to target, and which experiences to deliver.

  * **[User Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_user.htm&language=en_US&type=5)**  
A user trigger activates a campaign based on user behavior.

  * **[Catalog Triggers](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_types_catalog.htm&language=en_US&type=5)**  
A catalog trigger activates a campaign based on updates or changes to item
data in your catalog. The trigger activates after a change in your catalog,
but what drives the trigger is the amount of time the user views an item
before the catalog change occurs.

  * **[Filters for Triggered Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_filter.htm&language=en_US&type=5)**  
You can apply user behavior or catalog filters for some triggered campaigns to
refine qualification for trigger activation. A user behavior filter is based
on customer interaction with the trigger items. A catalog filter is based on
catalog attributes. For example, you can add a catalog filter to a product
back in stock trigger to have it activate only if the item price is less than
$100. Or, you can add a behavior filter so the trigger only activates if the
user favorites the product.

  * **[Trigger Frequency](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_trigger_frequency.htm&language=en_US&type=5)**  
Frequency limits apply to the number of triggers that Marketing Cloud
Personalization sends for a user profile for a specified time period.

  * **[Triggered Campaign Results](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_results.htm&language=en_US&type=5)**  
Marketing Cloud Personalization gives you insight into the performance of your
triggered campaigns.

  * **[Code Examples for Triggered Campaign Data in Marketing Cloud Engagement Emails](https://help.salesforce.com/s/articleView?id=sf.mc_pers_triggered_campaign_email_code_samples.htm&language=en_US&type=5)**  
Marketing Cloud Personalization sends recommendations and other trigger-
related catalog data, such as abandoned cart items, to Marketing Cloud
Engagement in JSON format. You can render the data in your Engagement emails
using Guided Template Language and Server-Side JavaScript. These code examples
show how to render triggered campaign data in an email recommendations block.

#### See Also

  * [Triggered Campaigns Use Cases](https://help.salesforce.com/s/articleView?id=sf.mc_pers_use_case_triggered.htm&language=en_US&type=5 "Drive impact through Triggered Campaigns, passing real-time information to Marketing Cloud Engagement. Check out these example personalization use cases that other customers have used in triggered campaigns.")

