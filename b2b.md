# B2B

Using [Tableau](https://www.tableau.com) as our "client", the following
document describes and presents code for an example implementation. The sample
code in this document is not exhaustive and maps only key areas of the site
that are valuable for demonstration purposes. The primary focus is depicting
how to approach designing a Catalog for B2B websites. While each
implementation is unique, this sitemap contends with many issues, particularly
mapping B2B sites and websites without purchasable products in general.

The sitemap code examples in this article are only for demonstration purposes.
Avoid copying sample code into your Sitemap Editor as it is built around
example scenarios that can differ from your implementation's goals and use
cases.

This section outlines the functionality that our imaginary client requires
from their implementation. Since each client or customer always has a unique
set of requirements and use cases in mind for Marketing Cloud Personalization,
experience is the real teacher when it comes to knowing what questions to ask
clients to help them establish their goals and requirements for their use of
Personalization.

  * Understand the content a user is most interested in based on their prior interactions with the site.

  * Recommend Blogs similar to recently viewed Blogs, fallback to promote trending Blogs.

  * Recommend Articles of the same Category (solutions, learn, or products) as the currently viewed landing page.
  * Personalize banner based on past interest in Articles under the currently viewed Category

  * Capture `Industry`, `JobRole`, `PageBundle`, and `Department` values as related catalog objects.

  * Capture `Keyword` values as a related catalog object.
  * Recommend related product Articles by `Keyword`.
  * Distinguish between `Add-On` and `Software` products in the Catalog.

  * Recommend trending `Blogs`.

  * Recommend related `Blog` posts based on category.

  * Since it is the only identity consistently available on the web and used as a username when users log in to the site, `emailAddress` is used as the default Web SDK identity attribute used for this implementation. The site already uses email addresses to identify its users, so we are configuring Personalization to piggyback on that identity attribute. 

> _**Aside** : Since an email address is Personally Identifiable Information
> (PII), make sure you have the appropriate approval from within your
> organization before using it as a Personalization Identity. Additionally,
> using emails captured from web forms, other than a login form, as an
> Identity could potentially cause privacy issues where more than one user is
> tied to a Personalization user. In the following code, email is only being
> captured from the login form when a user successfully logs in. The code
> capturing user id is designed to work on [Tableau
> Public](https://public.tableau.com/) as this portion of the Tableau site is
> accessible by everyone with a free public account. For more information on
> Identity, read [Identity System Setup for the Web
> SDK](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk.htm)._

  * While this site does promote products, there is no ability to purchase products or attribute revenue to them from other channels, matching with user activity from the web. Since we do not need the special capabilities of the `Product` item type for this implementation, we are instead using the `Article` item type, using `Category` to tell types of `Article` items apart. 

> _**Aside** : If the website had a more robust, hierarchical category system
> in which it could be possible to share `Category` information between the
> `Article` types, we would instead configure a catalog object specifically to
> house the type of `Article`, such as `ArticleType`. This way, if solutions
> and products shared `Category` data, they would be relatable to each other,
> instead of belonging to siloed `Category` hierarchies, each starting with
> their respective `Article` type (solutions, products, and learning)._

  * There is a categorization system already natively built into the site's blog section, so our code scrapes the categories already present in the `dataLayer` as `Category` in the Personalization Catalog. Collecting `Category` data for the `Blogs` help build user affinity based on those categories. These categories are used to also power the customer's use case to recommend related `Blogs` on blog pages based on the currently viewed `Category`.
  * In addition to `Category` data, the `dataLayer` contains other useful information, such as `Department` and `Job Role`. The values for `Department` and `Job Role` are collected as `relatedCatalogObjects` to tie them to each of the collected `Article` types. As these values are collected, they are used to build a user's affinity towards them, which can then be used for segmentation and potentially for recommending `Articles` of any `Category` based on one of these related catalog objects, instead of only recommending `Articles` of one type at a time.
  * To distinguish between `Add-On` and `Software` products in the Catalog, as stated in the "Client Requirements", we are mapping a related catalog object called `ProductType` on the "product" page type. Remember, we are using the `Article` item type to house Catalog data for the `product`, `solutions`, and `learning` page types. As a result, our `ProductType` catalog object is attached to the `Article` Catalog item type when configuring the Catalog, even though it is mapped only on one page type containing `Article` Catalog data. The `ProductType` related catalog object helps to more granularly distinguish which type of product `Article` is being viewed by the user and create highly targeted recipes based on that activity, if desired.

The following examples assume that `emailAddress` has been configured as the
default Web SDK Identity.

  * [_Salesforce Help_ : Identity System Setup for the Web SDK](https://help.salesforce.com/s/articleView?id=sf.mc_pers_identity_web_sdk.htm)

