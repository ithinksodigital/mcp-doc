

# Web Site Personalization

Integrate Marketing Cloud Personalization with your organization's web site.
During implementation, your development team works with Salesforce to create
your organization’s site map and plan your web integration.

The Marketing Cloud Personalization module of the Salesforce Interactions SDK
uses a JavaScript beacon to manage the flow of data between the
Personalization platform and the SDK libraries used in the client integration.

  * The Salesforce Interactions SDK is an extensible data capture and collection framework. Use it to track website visitors’ profile data and different user interactions on your website and send that information to Salesforce. The SDK consists of a base SDK and includes product-specific modules, one of which is the Marketing Cloud Personalization module.
  * The JavaScript beacon monitors and tracks the online behavior of your web users. When a user accesses your website, the JavaScript beacon places a first-party cookie on the user's browser, which sends data for that user back to Personalization. This data includes pages visited, links clicked, time on the site, the number of visits, geolocation, and the referral source, as well as other custom data you want to collect. 

![4c7f6efe-9973-4e2f-8a71-16af8442e406]

Note For web users who use ad blockers, an ad blocker set to highly
restrictive settings can block personalized experiences.

To integrate Personalization into your organization’s web site, see [Marketing
Cloud Personalization Web
Integration](https://developer.salesforce.com/docs/marketing/personalization/guide/web-
integration.html).

