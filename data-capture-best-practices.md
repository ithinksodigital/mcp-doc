# Best Practices for Data Capture Using Site Mapping

After reviewing all relevant sitemap documentation, move your sitemap from
your test dataset to your production environment only after thoroughly testing
and validating it. Additionally, the information in this document can prove
helpful to reference throughout each phase of implementation. As a final
validation for working on a sitemap, we suggest working through the following
steps.

The checklists laid out in this document are by no means comprehensive.
Instead, they call out common areas where implementors run into trouble while
writing sitemap code.

* * *

  * Validate the JavaScript
    * Checklist
  * Use the browser extension to test the sitemap code
    * Checklist
  * sendEvent function usage
  * Single Page App (SPA) sites
  * Timing issues
  * Data Capture Sources
    * Window Objects
    * Meta Tags
    * itemprop
    * JSON-LD
    * URLs
    * Page Source Code
      * Example
    * DisplayUtils
    * util.resolveWhenTrue
    * Additional Best Practices

* * *

  * Check for common JavaScript errors by reviewing the sitemap code in the sitemap code editor, found in the Personalization Visual Editor. The sitemap code editor helps identify and highlight errors in your code. You can also validate your code by visually spot-checking it for errors.

  * Depending on your chosen SDK namespace, use `SalesforceInteractions.cashDom` or `Evergage.cashDom` for each implementation instead of using jQuery or another library that the Personalization platform does not include (such as Knockout). Since the Personalization Beacon includes CashDom (the [`cash`](https://github.com/fabiospampinato/cash#documentation) library), code written using CashDom remains unaffected by updates made to JS libraries found on the client site, thus allowing for greater stability over time.

  * Ensure that the sitemap does not manipulate the DOM in any way; that is the function of the Campaigns and Templates system. For more information on using these features on your Web integration, see [About Web Campaigns and Templates](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign.htm) on Salesforce Help.

  * When using custom code to supply dates to the backend, ensure the custom code instantiates dates using `new Date(Date.UTC(YYYY, MM, DD))` instead of `new Date(YYYY, MM, DD)`. Using `new Date(YYYY, MM, DD)` can introduce errors due to differences between an end user's timezone and the way dates are stored as UTC.

  * Whenever possible, avoid using resolvers in situations where a direct value needs to be ingested since resolvers are designed to return a function. For example, the following examples depict improper use of a resolver.

  * Injecting or forcing the SDK URL to test the sitemap code. 
    * [Install the Salesforce Interactions SDK Launcher](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_interactions_sdk_launcher.htm)
    * If you followed the best practices detailed in the [Plan a Web Integration](/docs/marketing/personalization/guide/web-integration-planning.html) document, you can validate your sitemap code against an available test dataset.
  * After your test dataset runs on the site, click through the mapped pages and check to see that the events are sending as expected. 
    * Refer to our documentation on [Event Validation Using Chrome Browser Developer Tools](/docs/marketing/personalization/guide/sitemap-event-validation.html#event-validation-using-chrome-browser-developer-tools).

  * No errors in the **Network** tab for each event.
  * Mapped attributes are appearing as expected in the events.
  * Ensure that the [Sitemap Implementation](/docs/marketing/personalization/guide/sitemap-implementation.html) and any [Event API Request](/docs/marketing/personalization/guide/event-options-salesforceinteractions.html) objects in your code are appropriately structured and collect values of the correct type for each option, as described in the documentation for [Attributes](/docs/marketing/personalization/guide/attributes.html).
  * When collecting `Category` data associated with another item type (`Article`, `Product`, or `Blog`), ensure that the structure and case of category IDs are _exactly_ consistent on all catalog items mapped with categories.
  * Carefully validate category ID structures. When mapping the `Category` item type directly, ensure that the value of `id` (or `_id` in the `Evergage` namespace) in the `pageType` is _always_ supplied as a string. Additionally, you can construct a hierarchy of Categories by using `|` separated values to denote each level of the `Category` hierarchy. Ideally, these values are normalized in some way with your sitemap as they are collected. Normalizing these values helps ensure consistency within your catalog. For example, the Personalization platform considers a `Category` with a "Green Hats" ID different from a Category with a "Green hats" ID. In the following example `Category` ID, all the principles and best practices concerning `Category ID` structure have been used: `main-category|sub-cat-1|sub-cat-2`.
  * Check whether listeners are binding correctly on each page and are successfully sending events without errors or incorrectly formatted data. For example, if a sitemap has a click listener that listens for a button click to send an `AddToCart` event, ensure that clicking that button sends an `AddToCart` event with all the appropriate `lineItem` data successfully.
  * Validate that `onActionEvent` is being used correctly. While it is possible, we strongly discourage the use of event listeners and/or the `sendEvent` function in `onActionEvent`. However, if you do decide that you must use `sendEvent` here, take extra care to make sure that your code includes an exit case. Otherwise, you risk the possibility of triggering an infinite loop. Ensure that `onActionEvent` is not being used to overwrite the contents of the event, instead only to manipulate it and/or append additional data. Additionally, make sure that `onActionEvent` always returns the `ActionEvent`, even if no transformations and/or modifications are made. You can find examples of properly using `onActionEvent` to ingest user attributes in the [Capturing User and Account Attributes](/docs/marketing/personalization/guide/capturing-user-account-attributes.html) page.
  * Validate that your code is using supported and correctly formatted fields when mapping Page Types. The supported fields are outlined in the [Page Types](/docs/marketing/personalization/guide/page-types.html) documentation.
  * Ensure that your mapped content zones can serve the customer's use-cases. Refer to the [Content Zones documentation that outlines many commonly mapped content zones to get some ideas.

Depending on the SDK namespace you use, the following `sendEvent` function is
used to send an Event to Personalization. Ensure that events sent using this
function strictly follow the structure of the Event API requests, as outlined
in the [Event API](/docs/marketing/personalization/guide/event-api.html)
documentation.

While very similar, the Event API and page types in the sitemap _do_ have
different structures.

For more information about handling SPA page changes, refer to the [Single
Page App (SPA) Handling](/docs/marketing/personalization/guide/sitemap-
implementation.html#single-page-app-spa-handling) documentation. While using
an interval powers the documented example on that page, you can use a
different mechanism to monitor the site for page changes at your discretion.

  * Do selectors work in the console or editor, but the sitemap is still unsuccessful in scraping those values when sending the event?

    * The location of the data you are scraping probably does not exist at the time the page matches.

    * Solution:

      * Write a [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) for the `isMatch` function that matches the page type, which relies on data not available precisely at page load. The page is matched after the `Promise` resolves, that resolution being delayed until the source of your data exists in the DOM or `window` object.

If you do decide to use a Promise, ensure that you include a mechanism that
resolves the Promise after a set period, regardless of whether the match
condition has been met.

  * Does the catalog configuration work in the editor, but the sitemap is still unsuccessful in scraping those values when sending the event?

    * The catalog configuration values are being evaluated when the sitemap is parsed and not when the `pageType` is matched.

    * Solution:

      * Be sure to use custom functions or [`resolvers`](/docs/marketing/personalization/guide/sitemap-implementation.html#resolvers) for catalog configuration values. If you do not use functions or resolvers, these fields are evaluated when the browser parses the sitemap object, not when the `pageType` is evaluated.

      * For example:

When deciding on what to capture, first **consider all possible locations
where the data is available on the page for that`pageType`**. While testing a
new data source, ensure that the method of obtaining the data persists
throughout the Page Type and that the data is available when the sitemap
executes. For synchronous integrations, this could mean using a `Promise` to
resolve the `isMatch` function when data is available or using `Promises` for
the catalog ID field until the available data is available to capture.

Data found within window objects (that is, `window.dataLayer`) tends to be
more static and reliable, though be careful about using a third-party vendor.
Sites correctly implemented with Shopify, Magento, and Drupal tend to be more
reliable than others.

Taken from the [ecommerce
example](/docs/marketing/personalization/guide/ecommerce.html), we are able to
extract the product details found inside the ecommerce data object in the
following examples.

You can use the `SalesforceInteractions.resolvers.fromWindow` and
`SalesforceInteractions.mcis.getValueFromNestedObject` functions in the
`SalesforceInteractions` namespace and `Evergage.resolvers.fromWindow` and
`Evergage.util.getValueFromNestedObject` functions in the `Evergage` namespace
to return a value from a nested object safely.

For example, when capturing data from
`window.dataLayer[0].ecommerce.detail.products`, you could encounter an error
if one part of the path is not defined. The
`SalesforceInteractions.resolvers.fromWindow` function ( the
`Evergage.resolvers.fromWindow` function in the `Evergage` namespace) safely
navigates the given path to return a value if it exists or `null` if the
nested object, or some object in the path, does not exist.

If the data exists within the meta tag and the DOM, meta tag data is a
reliable data format. Personalization has a built-in resolver function in the
`SalesforceInteractions` and `Evergage` namespaces to retrieve data from meta
tags:

As an example, say a hypothetical website selling widgets contains the
following meta tag for description.

In a catalog configuration, you can retrieve the description content of that
tag with the following code.

`description` now has the string value: `The premier place for all your widget
needs.`

The `itemprop` attribute is used to add properties to an element on the page,
describing the content in the element. To learn more about the itemprop
attribute, refer to the [itemprop](https://developer.mozilla.org/en-
US/docs/Web/HTML/Global_attributes/itemprop) documentation on the [Mozilla
Developer Network](https://developer.mozilla.org/en-US/).

Depending on the SDK namespace you're using, Personalization has the following
built-in resolver function to retrieve data from elements with a specified
`itemprop`. This resolver function returns the content of the first matching
element with the given `itemprop`.

For example, when trying to capture the rating on a product, you could come
across a page that contains the following element:

In a catalog configuration, you can retrieve the rating value of that element
with the following code.

`rating` now has the value `"5"`

JSON-LD is a popular way to annotate and describe elements on a page with
structured data. Personalization has the following built-in resolver function
to parse and retrieve data from a JSON-LD element. This resolver function
parses the first JSON-LD script on the page. If given a `path`, it returns the
value of the path from the parsed JSON-LD object.

For example, if a site had the following element:

In the catalog configuration, you can retrieve the entire object using the
preceding resolver function. Alternatively, if you only wanted a single
element such as `name`, use the resolver function as shown in the following
examples to retrieve the entire object.

A page's URL can contain helpful information that you'd like to capture. For
example, you can capture a Product URL directly from the URL the user is
visiting using the following resolver function.

Some pages can also contain a canonical link element that is the preferred URL
of the page. You can capture canonical URLs using the following resolver
function.

Sometimes the only source of data is the DOM itself. Personalization has
several helper functions that can extract the data you need. The following
table lists the helper functions available in the `SalesforceInteractions` and
`Evergage` SDK namespaces that you can use to extract text and attributes from
elements in the DOM.

`SalesforceInteractions`| `Evergage`| Description  
---|---|---  
`SalesforceInteractions.resolvers.fromSelector`|
`Evergage.resolvers.fromSelector`| Retrieve data from an element.  
`SalesforceInteractions.resolvers.fromSelectorMultiple`|
`Evergage.resolvers.fromSelectorMultiple`| Retrieve data from multiple
elements.  
`SalesforceInteractions.resolvers.fromSelectorAttribute`|
`Evergage.resolvers.fromSelectorAttribute`| Retrieve attributes from an
element.  
`SalesforceInteractions.resolvers.fromSelectorAttributeMultiple`|
`Evergage.resolvers.fromSelectorAttributeMultiple`| Retrieve attributes from
multiple elements.  
  
Consider your website's sitemap code has the following element.

In the catalog configuration, you can retrieve the product ID with the
following code.

You can also retrieve the product's name with the following code.

If you're familiar with [cash](https://kenwheeler.github.io/cash/), you can
use `SalesforceInteractions.cashDom` (or `Evergage.cashDom` in the `Evergage`
namespace) to retrieve data on the DOM. You can view the list of available
utility functions in Evergage.js in the source menu inside the dev tool.

When you do have to use a Promise to wait for data to be available, the [web
template display utilities](/docs/marketing/personalization/guide/web-
template-display-utilities.html) provide methods that are helpful in waiting
for specific elements to be on the page. These methods trigger only when the
specified element is loaded on the page.

For example, if you need to wait for the `#productId` element to be on the
page in order to capture the ID of a product, you can use `pageElementLoaded`
utility as shown in the following examples.

When you have to wait for data to be available on the page, you can use the
following [utility function](/docs/marketing/personalization/guide/sitemap-
implementation.html#utility-functions) to bind and unbind processes that
return a Promise that resolves when the provided function returns a "truthy"
value.

The preceding function also supports a timeout that rejects the Promise if the
provided function does not return a "truthy" value within the specified time.
For example, if you need to wait for the `window.dataLayer[0].productId` to be
available on the page to capture the product ID, you can use the following
code.

  * **Avoid undefined data**
    * If your data field depends on a resolver, include it as a return inside a function to avoid sending undefined data.
  * **Practice console logging**
    * Get into a good habit of console logging the data in the sitemap. Just because it was available in Chrome Developer Tools doesn’t guarantee its availability at the precise moment that the Personalization sitemap code is executing. Consider the timing when the data is available. 
      * Does it load only after a specific action?
      * Is it only available when the user is logged in?
    * Only use console logging when developing a sitemap. Avoid including these statements in a live sitemap.
  * **Test your data source thoroughly**
    * Navigate to the page from a different link
    * Click back and forth on the browser button to ensure the data persists through the change.
    * Some pages can display differently depending on the referring source. This behavior is especially true for single-page applications.
  * **Consider backup plans**
    * If the data is available in two separate areas, consider using the second data source as a backup.
    * When creating custom helper functions, always assume the value is not available and null check everything.
  * **Ensure clean data capture**
    * Trim and clean the values, especially when it comes to IDs. Errant empty spaces can produce duplicate items in the catalog.
  * **Keep your data capture as simple as possible**
    * When using selectors, prefer IDs and unique classes over relative selectors if possible. Long chains of child selectors or selectors using `nth-child` may not always return the same element on pages of the same type.
    * When using selectors on the DOM, reduce the number of selectors to the minimum required to obtain the data.
    * If the selector is too specific, it could capture data incorrectly and differently from the way it does on other Page Types.
  * **Double-check data capture from meta tags**
    * Be careful of meta tags; some sites do not always update the meta tags appropriately.

  * [_Salesforce Help_ : Install the Salesforce Interactions SDK Launcher](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_interactions_sdk_launcher.htm)
  * [_Salesforce Help_ : About Web Campaigns and Templates](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign.htm)
  * [_External Link_ : Cash Documentation](https://github.com/fabiospampinato/cash#documentation)

