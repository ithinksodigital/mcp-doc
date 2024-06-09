

# About Open Time Email Campaigns

Email campaigns use an individual’s unique intent and preferences to deliver
true 1:1 personalized content, regardless of the email marketing or marketing
automation system. With Marketing Cloud Personalization open time email
campaigns, you can deliver up-to-the-second personalized content and
recommendations. Email messages can address a customer’s latest actions on
your site, include expiration date reminders, show low product inventory
levels, and more.

![38aa199d-6250-4b06-a069-16ac0c93a932]

Important At this time, localization isn’t supported for use with open time
email campaigns. Enabling localization in datasets used by open time email
campaigns can result in inconsistent and unexpected personalized content.

## Recommendations and Recommendation Calculation Interval

Creating an open time email campaign generates a block of HTML code that you
use in your existing email marketing service to add personalized content and
recommendations for each recipient. Personalization recalculates
recommendations after 1 hour. So, if a recipient opens an email and then
revisits that email within an hour with no other interactions, they see the
same recommendations. If they revisit the email after an hour, Personalization
recalculates the recommendations based on the recipe parameters, and the
recipient sees a different set of items.

## Expiration Time for Recommendations

You can change the expiration time that Personalization uses when
recalculating recommendations. For more information, see [Change the
Expiration Time for
Recommendations](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_recommendation_expiration.htm&language=en_US&type=5
"Recalculate recommendations that Personalization shows to users after a set
time has elapsed.").

## Recommendations in Apple Mail

For recipients that use Apple Mail, Personalization generates recommendations
at send time, rather than open time because of the way Apple handles requests.
Impression statistics for Apple Mail recipients calculate at send time.

## Open Time Item Templates

Before you can create a recipe-driven open time email campaign, you must
design an open time item template that controls how content and product
recommendations appear in your campaigns. You can have more than one template
and can customize templates, for example, to match your brand guidelines. Open
time item templates render as images to ensure that all items display in the
proper format, regardless of the email service or viewing device.

For more information, see [Build Open Time Item
Templates](https://help.salesforce.com/s/articleView?id=sf.mc_pers_email_campaign_template.htm&language=en_US&type=5
"Design and build templates for open time email campaigns.")

## Open Time Email Image Generation

When a template is published, an image generation job creates the initial set
of images for all items that match the item type of the template. These images
are stored on the Personalization CDN so that Personalization can deliver
personalized recommendations at email open-time.

Initial image generation job duration can vary based on the size of the
catalog. For example, a catalog with 1 million products takes longer than a
catalog with 100 thousand products.

If the error rate of the job exceeds 10%, the item template can’t be
published. Common example error causes include broken images on items or
missing attributes on items referenced in the template.

For troubleshooting information, see [Image Generation in Open Time Email
Campaigns](https://developer.salesforce.com/docs/marketing/personalization/guide/image-
generation-email-campaigns.html?q=images) in the Marketing Cloud
Personalization developer documentation.

## Open Time Email Image Updates

If an item is updated and the metadata referenced by an open time email
template changes, the item is queued for an image refresh. This refresh
ensures that the image on the Personalization CDN has the most up-to-date
information based on template requirements. The Personalization image refresh
sync runs every 10 minutes and batches items into groups of around 10
thousand.

![121f7bec-d872-41a9-9383-f4c01d53782b]

Note Over 10 thousand items can trigger a backup so that the system can catch
up.

It’s important to consider the rate at which item updates occur or are sent to
Personalization. Refer to the following example scenarios:

Scenario | description  
---|---  
Single Product Item Template | Imagine you send an ETL feed that updates 30 thousand products. Refreshing all of the images on the CDN would take around 30 minutes (assuming no additional item updates were received in that time via another source like the sitemap).  
Single Product Item Template | Imagine you send an ETL feed that updates 50 thousand products every 30 minutes. The image update queue in Personalization can outpace the image update sync. For optimal results, consider the frequency of item updates (via ETL, the sitemap, API, and so on) and how they relate to syncing updated images to the CDN.  
Multiple Product Item Templates | Imagine an item’s attributes are updated in a way that requires updates to multiple item templates (for example, five-item templates). This update counts as one update out of the 10 thousand. That is, it doesn’t multiply one item by the number of templates requiring updates. Five images must still be generated for that item. The update can be slower given the required processing for the five images.  
Item Templates of Multiple Types | Each eligible item type (for example, a product or article) has a 10 thousand image sync limit every 10 minutes.  
  
## Open Time Email Preview and Testing

You can access an Open Time Email Simulator Preview in the open time email
campaign editor. This preview allows you to search for an individual and
preview email recommendations. Images displayed in this view reflect the
images stored on the Personalization CDN. The simulator also uses a “cache-
buster” to generate a new call every time you select a user. A cache-buster
isn’t recommended in a live email campaign, as it prevents statistics
tracking.

If you want to compare results to those results returned in an email inbox,
it’s important to understand the following:

  * Browser Caching: When Personalization generates open time email images, a cache-control header is set for a maximum of five minutes. Browsers locally cache the image for that amount of time. If the recommendations are the same, the browser uses the image that is stored in local storage. If the item image changes in Personalization between initial open and browser cache expiration, a user can momentarily see a stale image because the browser hasn’t yet contacted Personalization.

  * Third-Party Caching: Certain mailbox providers use additional internal image caching on top of the browser cache. This internal caching can affect the refresh rate of open time email images. It doesn’t affect the actual recommendation decision but can affect the image displayed for an item. Personalization can’t validate or verify the differences in caching across mailbox providers.

You can also refresh images for an open time email item template on the item
template edit screen. With this preview, enter an item ID and preview how the
image would look if the image were generated at that moment. The image
displayed in this preview might not match what is stored on the CDN. The
update to the image on the CDN could still be in progress. If there appears to
be a mismatch, wait for any active image syncs to complete and validate the
image on the CDN later.

With an item image preview on the Personalization CDN, you can see which image
is stored in the CDN for a given template and item. To preview an item image,
enter the following URL, replacing the capitalized variables with relevant
values. Only items that match the item type of the template display an image.
The image displayed by this link is the image a customer sees when they open
an email based on the item template.

https://cdn.evergage.com/blocks/{ACCOUNT_ID}/{DATASET_ID}/{ITEM_TEMPLATE_ID}/{ITEM_ID}.png

To find the ID of an item template, select Email > Open Time Item Templates,
click the three vertical dots of a column header, and select the ID option.

#### See Also

  * [ _Developer Documentation_ : Image Generation in Open Time Email Campaigns](https://developer.salesforce.com/docs/marketing/personalization/guide/image-generation-email-campaigns.html?q=images)

