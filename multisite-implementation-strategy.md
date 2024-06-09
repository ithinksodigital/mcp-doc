# Multisite Implementation Strategy

Marketing Cloud Personalization accounts are similar to Marketing Cloud
tenants - customers typically sign up for a single account for their license
and can have multiple datasets associated with each account.

Each dataset in Personalization is a separate, siloed data environment. As
datasets don’t share data among themselves, the same user could have an
independent profile in each dataset. Campaigns, segments, statistics, and
integrations are also not shared between datasets. Personalization customers
can also set permissions levels for their teams, ensuring that each team has
access to the datasets they need in order to use Personalization for their
business needs.

It’s common to have a single dataset associated with one web domain. However,
it’s possible to have more than one domain on a Personalization license or a
domain serving multiple countries in multiple languages. In these cases,
dataset design during the discovery process is essential in a successful
Personalization implementation.

  * How many web domains does the license include? Are they all the same brand, or are they different brands?
  * How many countries (or locales) does the domain support?

![fbe1bd5f-f383-45d6-a5f0-795d7fa52788]

If there are multiple domains on one Personalization license, either maintain
a separate dataset for each domain or combine the domains into a single
dataset. Often, it’s best to have a single dataset per domain, but there are
good reasons to combine multiple domains into a single dataset. The following
sections provide guidance on using a single dataset for multiple domains.

Depending on the catalog differences between the different sites, there are
some things to consider when designing the catalog data model. If the sites do
share products with identical IDs, it’s advisable to differentiate between
these products by making the IDs unique per site. You could do so by prefixing
the IDs that a unique identifier for the site would capture.

For example, consider two sites, `https://foo.example/` and
`https://bar.example/`. These two sites share a product with the ID `abc123`.
When importing and capturing catalog data, you could prefix this product ID
based on the site to differentiate the product in the Personalization Catalog
since it could have different attributes depending on the site. On
`https://foo.example/`, the ID could become `foo_abc123`, and on
`https://bar.example/`, the ID could become `bar_abc123`.

To help differentiate products that exist on different sites in the same
dataset, it’s a good idea to track a related catalog object for the site the
product appears on. This related catalog object would allow for
differentiating products available only on the site the user is on in recipes.
Consider the two sites `https://foo.example/` and `https://bar.example/`. When
viewing a product on `https://foo.example/` you could set this related catalog
object to `foo.example` and when viewing a product on `https://bar.example/`
you could set this related catalog object to `bar.example`. Having this
related catalog object available would allow adding a recipe exclusion to any
recommendations so that only products available on the site the user is on
would be recommended.

When mapping multiple sites to the same dataset, these sites share the Web SDK
and Sitemap integration.

By default, the current domain is set as the `cookieDomain` when initializing
the Web SDK. To configure the `cookieDomain` setting, you must dynamically
determine which domain to set the cookie on since different sites share the
initialization.

The following examples show how to dynamically determine and set a custom
`cookieDomain` based on the site where the Web SDK is initializing. The
Personalization Web SDK anonymous user IDs are generated separately for each
domain. When integrating multiple domains in the same dataset, users tracked
anonymously are tracked as separate users across the different domains.

When mapping multiple domains to the same dataset, it’s good practice to have
separate Sitemap configurations for each domain if the Page Types and Content
Zones defined share names but capture different Interactions. Having Page
Types and Content Zones share names makes it possible to share templates and
campaigns between the domains. Moreover, if you don't use the same Content
Zone names and Page Types, the template editor only shows options for the last
domain that the Sitemap was saved for in the Visual Editor.

After you have built the Sitemap configurations for each domain, you must
initialize the correct Sitemap configuration based on the domain the user is
visiting currently.

The following examples depict a configuration that initializes the correct
Sitemap for the domain a user is visiting currently.

If multiple sites have different Page Types and Content Zones, another method
is to use one Sitemap configuration for all domains. With this method, each
`pageType` must have logic in its `isMatch` function to determine whether to
match for the current page and domain.

The following example depicts using a single Sitemap configuration matching on
multiple domains.

To use different Sitemap configurations for multiple domains, keep the same
`pageType` names for equivalent pages on different domains. You can
differentiate which site the user is visiting using Interactions and Catalog
Objects. For example, a product detail page on `https://foo.example` and a
product detail page on `https://bar.example` must share the same
`product_detail` Page Type.

For Content Zones, use consistent names across domains to make it easier to
share templates and campaigns. You can, however, have different Content Zone
selectors across domains.

If you don't use the same Content Zone names and Page Types, the template
editor only shows options for the last domain that the Sitemap was saved for
in the Visual Editor.

