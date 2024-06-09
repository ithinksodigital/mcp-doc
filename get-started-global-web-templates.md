# Get Started with Global Web Templates

The simplest way to develop a Marketing Cloud Personalization web template is
to use one of our global templates and customize it for your business use
case. To use a global template, do the following.

  1. Clone the global template that most closely represents your web channel use case.
  2. Customize the template based on business user requirements.

The following sections present the steps for cloning a global template in
Personalization and the standards for customizing global template code.

For information on the most current list of available global templates and
their recommended web channel use cases, see [Web Campaign Template
Properties](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_properties.htm)
on Salesforce Help.

To clone a global template, do the following:

  1. Open the [Salesforce Interactions SDK Launcher](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_interactions_sdk_launcher.htm) Chrome extension tool, and click the **View List** section of the template button:

![ce70fe68-86b1-4042-af83-a6041afb6301]

  2. To find a list of all currently available global templates, click the **Global Templates** tab.

  3. To clone a global template for customization, click the **Clone Global Template** button associated with the global template you want to customize.

![fc9debe3-0cfa-4d25-bfa5-4d25f09ace08]

  4. Cloning a global template opens a new copy of the template, with the text "[CLONE]" prepended to the template name.

Cloning and customizing a global template doesn’t alter the original version
of the global template in the **Global Templates** tab. You can make as many
clones of a global template as you require for different use cases.

![a854145e-2711-4929-8dce-590a7ae1e69e]

In global templates, comments are provided at the top of the code tabs to help
template developers effectively customize the template. For an example of
comments within global templates, see the comments in the **Handlebars** tab
in the above **[CLONE] Einstein Product Recommendations** figure.

  5. Click **Save** to save the cloned version of the global template to your dataset. This cloned version appears in the **Templates** tab along with any other templates you’ve created or cloned.

![47936e4c-ecbe-4ce0-9369-cedebe5a1faa]

After you’ve cloned a global template as described in the preceding section,
customize the template components to meet the requirements of the business use
case. As a best practice, we recommend you modify the template component code
in the following order:

  1. Modify the server-side code in the **Serverside Code** tab. See [Web Template Server TypeScript](/docs/marketing/personalization/guide/template-server-typescript.html) for more detail.
  2. Modify the client-side code in the **Clientside Code** tab. See [Web Template Client JavaScript](/docs/marketing/personalization/guide/template-client-javascript.html) for more detail.
  3. Develop the Handlebars templated HTML code in the **Handlebars** tab. See [Web Template Handlebars](/docs/marketing/personalization/guide/web-template-handlebars.html) for more detail.
  4. Develop the CSS style code in the **CSS** tab. See [Web Template CSS](/docs/marketing/personalization/guide/web-template-css.html) for more detail.

When customizing global templates, follow the recommendations outlined in the
following articles.

  * [Web Template Building Best Practices](/docs/marketing/personalization/guide/web-template-building-best-practices.html) provide an outline of standards for building templates that run optimally on your website.
  * [Web Templates Style Guide and Coding Conventions](/docs/marketing/personalization/guide/web-templates-style-guide-and-coding-conventions.html) provide a guide to writing consistent template code.

  * _Salesforce Help_ : [Web Campaign Template Properties](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_template_properties.htm)
  * _Salesforce Help_ : [Install the Salesforce Interactions SDK Launcher](https://help.salesforce.com/s/articleView?id=sf.mc_pers_web_campaign_interactions_sdk_launcher.htm)

