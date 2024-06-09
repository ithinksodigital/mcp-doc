# Financial Services

The following code sample depicts sitemap code for an imaginary implementation
of Marketing Cloud Personalization on the Cumulus Financial Services website
`https://www.cumulusfinserv.com/`. This sitemap code isn’t exhaustive and maps
only key areas valuable for demonstrating an example implementation of
Personalization. The primary focus of this sitemap code is to depict how to
approach designing a Catalog for websites offering financial services.

For financial services implementations, we recommend using the Product catalog
type as showcased in this example. In order to use this catalog type, we add a
default price and quantity for each Product when creating line items as that
data is not typically present on financial services Product Detail Pages
(PDPs). Then on the forms associated with PDPs, we create a checkout flow and
fire a `Purchase` interaction when the last step of a form is clicked. We
don't recommend using a custom catalog object type as it doesn't as easily
allow for conversion tracking. It's also harder to illustrate ownership when
using a non-Product catalog type.

The sitemap code examples in this article are only for demonstration purposes.
Avoid copying sample code into your Sitemap Editor as it is built around
example scenarios that can differ from your implementation's goals and use
cases.

