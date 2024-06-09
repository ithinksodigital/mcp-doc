

# FAQs for Open Time Email Campaigns

Refer to the following frequently asked questions about open time email
campaigns.

## How often does Marketing Cloud Personalization recalculate open time email
recommendations?

Personalization recalculates recommendations after 1 hour. For more
information, see “Recommendation Calculation Interval” in [About Open Time
Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_about.htm&language=en_US&type=5
"Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more.").

## Can I set an expiration time for open time email recommendations?

Yes. You can change the expiration time that Personalization uses when
recalculating recommendations. For more information, see [Change the
Expiration Time for
Recommendations](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_recommendation_expiration.htm&language=en_US&type=5
"Recalculate recommendations that Personalization shows to users after a set
time has elapsed.").

## Does using Apple Mail affect how recommendations are generated?

Because of the way Apple handles requests, Personalization generates
recommendations at send time, rather than open time. For more information, see
“Recommendations in Apple Mail” in [About Open Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_about.htm&language=en_US&type=5
"Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more.").

## How does Open Time Email handle image generation?

When an open time item template is published, an image generation job creates
the initial set of images for all items that match the item type of the
template. For more information, see “Open Time Email Image Generation” in
[About Open Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_about.htm&language=en_US&type=5
"Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more.").

## How often does Marketing Cloud Personalization update an image for an item?

If an item is updated and the metadata referenced by an open time email
template changes, the item is queued for an image refresh. There are
considerations for the rate at which item updates occur or are sent to
Personalization.

For detailed information, see “Open Time Email Image Updates” in [About Open
Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_about.htm&language=en_US&type=5
"Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more."). For information about troubleshooting issues, such as
missing or blurry images, see [Image Generation in Open Time Email
Campaigns](https://developer.salesforce.com/docs/marketing/personalization/guide/image-
generation-email-campaigns.html) in the Marketing Cloud Personalization
developer documentation.

## Can I preview an open time email campaign?

You can access an Open Time Email Simulator Preview in the open time email
campaign editor. This preview allows you to search for an individual item and
preview email recommendations. You can refresh images for an open time email
item on the item template edit screen. With an item image preview on the
Personalization CDN, you can see which image is stored in the CDN for a given
template and item.

For more information see “Open Time Email Testing and Preview” in [About Open
Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_about.htm&language=en_US&type=5
"Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more."). For troubleshooting information, see [Image Generation in
Open Time Email
Campaigns](https://developer.salesforce.com/docs/marketing/personalization/guide/image-
generation-email-campaigns.html) in the Marketing Cloud Personalization
developer documentation.

## Why do I see an image in the simulator that is different than in the actual
email?

Browser and third-party caching can affect the refresh rate of open time email
images. For more information see “Open Time Email Testing and Preview” in
[About Open Time Email
Campaigns](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_about.htm&language=en_US&type=5
"Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more."). For troubleshooting information, see [Image Generation in
Open Time Email
Campaigns](https://developer.salesforce.com/docs/marketing/personalization/guide/image-
generation-email-campaigns.html) in the Marketing Cloud Personalization
developer documentation.

## Can I use localization in my Open Time Email campaigns?

At this time, localization isn’t available to use with Open Time Email
campaigns.

