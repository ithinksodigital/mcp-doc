# Personalization Template System

Marketing Cloud Personalization's template system, composed of Web Templates &
Server-Side templates, provides developers with the ability to customize and
configure templates to support their business user's use case needs. A
template developer has complete control over each component of the template
and can determine which aspects of the campaign experience a business user can
manipulate. After a developer publishes a template for a business user to use
in a campaign, it becomes a reusable tool in the business user's optimization
arsenal that allows a business to test and learn at speed.

While developers can configure custom templates from scratch, Personalization
accounts are equipped with various global templates specifically designed to
cover some of the most common and powerful use cases. These templates require
minimal edits to leverage out of the box or can act as the starting point for
new template creation. The global templates are great use case accelerators
and living/breathing examples of template code in action.

For more information on global templates, see [Web Campaign Template
Properties](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_properties.htm)
on Salesforce Help.

Personalization has two types of templates available for developers to
configure.

  * **Web Templates:** Web templates consist of four essential parts: Server-Side Code, Client-Side Code, Handlebars, and CSS. They are used when the Personalization module of the Salesforce Interactions SDK is responsible for rendering the campaign experience on the client's site. Web templates also leverage the web content zones mapped during the website implementation. They determine where a campaign can render on the website.
  * **Server-Side Templates:** Server-side templates only use server-side code and are used to pass a JSON payload with customer or campaign response data for another system to consume and render.

Data that we refer to as the `context` drives the content displayed in
templates. The data in the `context` is derived server-side by Personalization
from the configuration of the campaign that is using the template. After it is
derived on the server, the `context` is passed to the client browser, where
the client-side JavaScript can choose what to do with it, including joining
the `context` with the HTML and rendering it.

The following documents include information and instructions on approaching
each component of a template.

  * [Template Handlebars](/docs/marketing/personalization/guide/web-template-handlebars.html)
  * [Template CSS](/docs/marketing/personalization/guide/web-template-css.html)
  * [Template Client JavaScript](/docs/marketing/personalization/guide/template-client-javascript.html)
  * [Template Server TypeScript](/docs/marketing/personalization/guide/template-server-typescript.html)

Personalization provides several [pre-built global
templates](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_properties.htm)
for common personalization use cases. Examples of pre-built global templates
include hero banners, popups, product recommendations, info bars, and so on.
These templates are highly customizable to suit individual needs and can save
developers a significant amount of time over creating a template from scratch.
New global templates are being developed and released regularly to meet a
variety of web channel campaign use cases.

To use a global web template, do the following.

  1. Choose the global template that most closely matches your business use case.
  2. Clone the template.
  3. Modify the template code to meet business requirements.

For developer guidance in completing the preceding tasks and best practices
for working with global web templates, refer to the [Get Started with Global
Web Templates](/docs/marketing/personalization/guide/get-started-global-web-
templates.html) documentation.

  * [_Salesforce Help_ : Web Campaign Template Properties](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_properties.htm)

