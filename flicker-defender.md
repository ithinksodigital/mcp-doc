# Flicker Defender

The Flicker Defender gear can help prevent flicker caused by the rendering of
personalized content (Templates/Campaigns) served by the Marketing Cloud
Personalization platform.

Flicker Defender helps prevent flicker by doing the following.

  * Initially hides every content zone that has a `selector` by temporarily applying the `visibility: hidden !important` style to elements targeted by that `selector`
  * Each hidden content zone is then redisplayed depending on: 
    * If it is not targeted by a Template/Campaign for which the user has qualified
    * Upon resolution of the Template/Campaign targeting it
    * When the `redisplayTimeout` is hit
  * If a page is not matched or if the Sitemap errors, all hidden content zones are redisplayed following the `pageMatchTimeout`

While there is no limit for either of the timeout values, it is advised to
stay under 10000 ms (10 seconds). Additionally, ensure that `pageMatchTimeout`
is less than or equal to the `redisplayTimeout`, since `redisplayTimeout`
ultimately decides when to reshow all hidden content.

* * *

For Flicker Defender to work correctly, ensure you meet the following
requirements.

  * A synchronously integrated Beacon in the `head` of the site is a strict requirement for Flicker Defender to work correctly.
  * A working sitemap is necessary for Flicker Defender to work correctly and efficiently. For information on writing a Sitemap, see the [Web Integration](/docs/marketing/personalization/guide/web-integration.html) documentation.
  * At least one Content Zone with a `selector` attribute. _(Note that it is the developer's responsibility to ensure that the CSS selector used is valid.)_

* * *

The following Flicker Defense timeout options are configurable from within
Site-Wide JavaScript.

`pageMatchTimeout` controls the maximum length of time to wait for a page to
be successfully matched before reshowing all hidden content

`redisplayTimeout` controls the maximum length of time that content should
ever be hidden.

Depending on the namespace you're using, calls to `setPageMatchTimeout` and/or
`setRedisplayTimeout` must be done before the call to either
`SalesforceInteractions.init()` or `Evergage.init()` in Site-Wide JavaScript.

  * By design, Flicker Defender does not run in the Template or Campaign Editors.
  * Depending on the SDK namespace you're using, ensure that you call `SalesforceInteractions.init` and `SalesforceInteractions.initSitemap` or `Evergage.init` and `Evergage.initSitemap` as soon as possible in Site-Wide JavaScript, since Flicker Defender relies on those calls to determine when to begin hiding content zones.
  * When injecting or forcing the Web SDK URL using the Salesforce Interactions SDK Launcher browser extension, you are simulating an asynchronous implementation of the product. Therefore, at least a small amount of Flicker always appears when injecting or forcing a Web SDK onto the page.

To effectively disable the Flicker Defender gear, add the following to the top
of your sitewide JavaScript.

