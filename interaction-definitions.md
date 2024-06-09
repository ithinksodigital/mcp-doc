# Interaction Definitions

The Salesforce Interactions SDK provides interactions names used to identify
certain user interactions related to `Catalog`, `cart`, and `order` objects.

Interactions contain a reserved `name` property and value that Personalization
uses to determine how to treat event data.

The Interactions documented in this article are available exclusively in the
`SalesforceInteractions` namespace. In the `Evergage` namespace, Interactions
are called Item Actions. For more information, refer to the [Item
Actions](/docs/marketing/personalization/guide/item-actions.html)
documentation.

An example of an event sent using the API within the Sitemap can be found in
our [Example ecommerce
Sitemap](/docs/marketing/personalization/guide/ecommerce.html) within the
`"product_detail"` pageType configuration. The following code sample includes
the relevant code block. In this example, a listener has been mapped
containing an `AddToCart` event that fires when the user clicks the DOM
element referenced by the provided selector, `".add-to-cart"`.

When tracking Catalog Object Interactions, Cart Interactions, or Order
Interactions, you have to reference all values assigned to the
`interaction.name` property from the `SalesforceInteractions` object. The
`SalesforceInteractions` namespace provides the following objects.

  * `SalesforceInteractions.CatalogObjectInteractionName`
  * `SalesforceInteractions.CartInteractionName`
  * `SalesforceInteractions.OrderInteractionName`

  * `SalesforceInteractions.CatalogObjectInteractionName.QuickViewCatalogObject` \- Similar to `CatalogObjectInteractionName.ViewCatalogObject` but stops the timer for the "background" item and starts a timer for the "foreground" item.
  * `SalesforceInteractions.mcis.CatalogObjectInteractionName.StopQuickViewCatalogObject` \- Stops the timer initiated by the "Quick View Item" interaction for the "foreground" item and restarts the timer for the "background" item.

`QuickViewCatalogObject` and `StopQuickViewCatalogObject` are used to
accurately track view time in cases where a user "views" an item while already
viewing a different item. An ecommerce category page that allows users to view
individual products in a window can take advantage of these interactions. In
the following example, the "background" item is the category and the
"foreground" item is the product. A new page load stops both timers.

Only the `interactions` documented here are currently supported. Unless
otherwise indicated, the following definitions apply to both the page config
and Event API.

Personalization accepts OrderInteractions other than the Purchase
OrderInteraction but only the Purchase OrderInteraction updates a user's order
in Personalization.

When using interactions, it’s important to keep the following best practices
in mind:

  * Only track interactions if they're necessary for personalization and targeting. Think about the personalization use cases you wish to execute and only map the interactions required for those specific use cases.
  * Map no more than a few thousand unique interactions per dataset. Mapping any more leads to challenges when using the Personalization UI, including difficulties in selecting interactions from dropdown menus and slower report generation.
  * Ensure interaction names have values you can reuse across users and sessions.
  * When defining interaction names, avoid dynamically populating them to prevent inflated names with unexpected prefixes and suffixes.
  * If you dynamically populate interaction names, ensure they stay consistent across sessions for any user.
  * Refrain from automatically sending all events from other site analytics tools to Personalization, as it can result in a higher volume of events than necessary for personalization.
  * Incorporating dynamic user information in interaction names can cause issues and must be avoided whenever possible.

