

# UTM Parameter Mapping

UTM parameters are customizable codes that you use in URLs and links to track
and measure the success of various aspects of your third-party campaigns. UTM
parameters can track traffic, referral sources, external campaigns, keywords,
and content zones.

## UTM Parameters

Use these standard UTM parameters.

Parameter | Description  
---|---  
utm_campaign | Identifies the campaign.  
utm_medium | Identifies the medium, such as a search engine, a social media platform, or another platform.  
utm_source | Identifies the source of the traffic, such as Google or AdWords.  
utm_term | Identifies keywords that generate clicks.  
utm_content | Identifies the content zone, such as a call-to-action message.  
  
## Campaign Match Configuration

When you have more than one third-party integration, it's important to define
the campaign match configuration so that Personalization can identify the
external campaign from each third-party product. Personalization looks at this
rule first, which is based on the event's landing page URL or the referrer
URL.

For example, a landing page URL for a Google AdWords campaign can look similar
to the following:

`https://www.yourcompany.com/landing/?utm_source=google&utm_medium=cpc
&utm_campaign=AwesomeAdWordsCampaign&gclid=CKSDxc_qhLkCFQyk4AodO24Arg`

To map this URL to an external campaign, you specify which marketing product
produced the campaign. Looking at the example URL, the `utm_source=google` and
`gclid=CKSDxc_qhLkCFQyk4AodO24Arg` query parameters indicate that the visitor
came to the page through an AdWords campaign.

So, for this example, you select or enter the following options in Campaign
Match Configuration:

Item | Description  
---|---  
Landing Page URL Query Parameter | the parameter type  
`gclid` | the query parameter  
matches regex | Matches the regular expression gclid  
.+ | Includes at least one character  
  
## Parameter Mappings

UTM parameters capture additional information about your third-party
campaigns. Mapping the UTM parameters tells Personalization how they
correspond to attributes of a Personalization external campaign, or to
attributes defined for the referred visitor. You configure how Personalization
interprets the UTM parameters in the links in your third-party campaign so
that they map to the correct fields in campaign analytics and reporting. When
mapping, be sure to specify whether the UTM parameters are in the landing page
URL or in the referral URL.

Target types to use in UTM parameter mapping include the following:

Item | Description  
---|---  
Campaign ID | The value of the query parameter becomes the Personalization external campaign ID. For an AdWords campaign with autotagging enabled, the gclid parameter is ideal for mapping to the campaign ID. For other types of campaigns, the utm_campaign parameter or the utm_content parameter can often be used. You must have at least one campaign ID mapping.  
Campaign Name | The value of the query parameter becomes the name of the Personalization external campaign. If there isn’t a campaign name mapping, the name defaults to either the value of the utm_campaign parameter, if set, or the campaign ID.  
Campaign Source | This value, such as `google` or `exacttarget`, typically maps to the utm_source parameter.  
Campaign Medium | This value, such as `cpc` or `email`, typically maps to the utm_medium parameter.  
Campaign Experience ID | The value of the query parameter becomes the campaign experience ID.  
Campaign Attribute | A custom attribute to set for the Personalization external campaign.  
User Attribute | A custom attribute to set for the Personalization user who clicks the external campaign.  
  
![351a784c-7d6a-44f3-b115-11c15466e943]

Note Don’t use identity attributes for this mapping. Capture identity
attributes through the site map.

