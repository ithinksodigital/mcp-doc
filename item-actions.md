# Item Actions

The `itemAction` property of the Salesforce Interactions SDK is used to
identify actions users take on catalog items such as "Purchase" or
"AddToCart".

Item actions are a separate event property from regular actions (`action`).
Item actions contain reserved action names used by Marketing Cloud
Personalization to determine how to handle event data. Personalization
automatically inserts the appropriate `itemAction` value when sending events
containing catalog data originating from matching a `pageType` mapped in the
Sitemap code. Therefore, avoid manually mapping the `itemAction` property in
your `global` or `pageType` configurations, except in the following scenarios.

When mapping pages with `cart` or `order`, you must specify `itemAction` in
your `pageType` configuration. Typically the `cart` object is mapped only on
the cart page itself with the `itemAction` value of "View Cart"
(`Evergage.ItemAction.ViewCart`). Similarly, `order` is only mapped on the
order confirmation page with the `itemAction` value of "Purchase"
(`Evergage.ItemAction.Purchase`). If no `lineItem` is provided with the
Purchase ItemAction, the SDK defaults to using the current state of the cart
as line items.

The Item Actions documented in this article are available exclusively in the
`Evergage` namespace. In the `SalesforceInteractions` namespace, Interactions
replace Item Actions. For more information, refer to the [Interaction
Definitions](/docs/marketing/personalization/guide/interaction-
definitions.html) documentation.

The `action` property is also used to track user interactions but isn’t
specific to actions carried out on catalog items. The purpose of `action` is
to provide a high-level overview of user behavior and to help identify trends
or patterns in how users interact with a website or application. For example,
you can use actions to track when a user views the home page or clicks a call
to action.

You can also use actions for the following purposes:

  * Segmentation: You can use actions as criteria to create user or audience segments. You can then target these segments to deliver personalized experiences, offers, or content based on their actions.
  * Campaigns: By using actions for campaign targeting, you can qualify users who have either performed or not performed a specific set of actions.
  * Actions Report: The Actions Report provides insights into user actions and user behavior over time within a given dataset, allowing marketers to identify key activities that are valuable for campaign targeting.
  * Funnels: You can also use actions to track user progression through funnels. By mapping actions to each funnel step, you can track and analyze user behavior and identify steps where users drop off or encounter obstacles. Such insight can help optimize user journeys and improve conversion rates.

When using actions, it’s important to keep the following in mind:

  * Only track actions if they're necessary for personalization and targeting. Think about the personalization use cases you wish to execute and only map the actions required for those specific use cases.
  * Map no more than a few thousand unique actions per dataset. Mapping any more leads to challenges when using the Personalization UI, including difficulties in selecting actions from dropdown menus and slower report generation.
  * Ensure action names have values you can reuse across users and sessions.
  * When defining action names, avoid dynamically populating them to prevent inflating names with unexpected prefixes and suffixes.
  * If you dynamically populate action names, ensure they stay consistent across sessions for any user.
  * Refrain from automatically sending all events from other site analytics tools to Personalization, as it can result in a higher volume of events than necessary for personalization.
  * Incorporating dynamic user information in action names can cause issues and must be avoided whenever possible.

The item action property value must be manually set only when sending events
to the Personalization platform using the Event API. Only the reserved item
action values within `Evergage.ItemAction` can be used. Within the context of
the Sitemap, the Event API is used to send an event independently of the page
matching event using `Evergage.sendEvent()`.

An example of an event sent using the API within the Sitemap can be found in
our [Example ecommerce
Sitemap](/docs/marketing/personalization/guide/ecommerce.html) within the
`"product_detail"` pageType configuration. The following code sample includes
the relevant code block. In this example, a listener has been mapped
containing an `AddToCart` event that fires when the user clicks the DOM
element referenced by the provided selector, `".add-to-cart"`.

The possible values for item action are all contained within the
`Evergage.ItemAction` object. Be sure to reference all values assigned to the
`itemAction` property from the `Evergage.ItemAction` object in the same way as
the `AddToCart` event detailed in the previous section.

  * `Quick View Item` \- Similar to `View Item` but stops the timer for the "background" item and starts a timer for the "foreground" item.
  * `Stop Quick View Item` \- Stops the timer initiated by the "Quick View Item" item action for the "foreground" item and restarts the timer for the "background" item.

You can use the `Quick View Item` and `Stop Quick View Item` item actions to
accurately track view time in cases where a user "views" an item while already
viewing a different item. An ecommerce category page that allows users to view
individual products in a window can take advantage of these item actions. In
the following example, the "background" item is the category and the
"foreground" item is the product. A new page load stops both timers.

While other Item Actions are present in the `Evergage.ItemAction` object, only
the Item Actions documented here are currently supported. Unless otherwise
indicated, the following definitions apply to both the page config and Event
API.

Many item actions mentioned in the following definitions rely on events that
contain line items. To learn more about the structure of the `lineItem`
object, see the [LineItem](/docs/marketing/personalization/guide/sitemap-
implementation.html#lineitem) documentation.

When using this specific action, only one item is updated at a time. A single
`AddToCart` event doesn’t accept an array of items. If you want to add
multiple items to the cart, the items must be sent in multiple events.

A `viewCart` event fully updates the items that a user has in their cart. For
example, sending a `viewCart` event via the Event API overwrites any items
currently saved in the user's cart.

**Sitemap PageType Definition**

**Event API**

**Sitemap PageType Definition**

**Event API**

When using this specific action, only one item is updated at a time. A single
`UpdateLineItem` event doesn’t accept an array of items. If you want to update
multiple cart items, you must send in multiple events.

The `RemoveFromCart` item action only removes one line item from the cart at a
time. A single `RemoveFromCart` event doesn't accept an array of line items.
To remove multiple cart items, you must send in multiple events.

The following example depicts how you can use the `RemoveFromCart` item action
to remove a line item from a shopping cart.

