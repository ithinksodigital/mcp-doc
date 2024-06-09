# Marketing Cloud Personalization Event API

The Marketing Cloud Personalization Event API allows sources to send event
data to the Personalization platform to be processed in the event pipeline,
which then returns Campaigns that can be served to the end user. The Event API
also allows for authenticated requests, returning internal Campaign data.

Don’t use the Event API to handle mobile application events. The
Personalization [Mobile SDK](/docs/marketing/personalization/guide/mobile-
integration.html) has separate functionality used for mobile app event
processing, with built-in features that are currently unavailable through the
Event API.

The [Event API Requests](/docs/marketing/personalization/guide/event-api-
requests.html) article in this section specifies standard HTTP methods and
JSON-formatted objects that can be used in the Sitemap and other
Personalization event sources to interact with the Personalization platform.

