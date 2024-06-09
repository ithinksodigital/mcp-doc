

# Manage Catalog Localization

You can localize catalog settings, including the language and currency that
your site uses, and the catalog metadata. You can define a primary locale and
primary currency for each dataset. The primary locale is the dataset’s default
locale.

### Required User Permissions

Permissions Needed  
---  
To edit catalog settings: | A role with Catalog Create/Edit permissions  
  
  1. From the main navigation, select **Settings** | **Catalog and Profile Objects**.
  2. For**Primary Locale** , select the language that Personalization uses to record your data.

If a locale value isn’t specified on an inbound event, the item data
associated with the dataset’'s default locale is returned in personalization
experiences.

  3. For **Primary Currency** , select the currency that you want to use for formatting, statistics tracking, and attribution analysis. When selecting the primary currency, keep these considerations in mind.

All monetary data is tracked using the selected primary currency value. For
example, if **euro** is the primary currency value, Personalization tracks and
records all purchase and conversion data in euros, and all UI references to
money appear in euros.

Changing the currency setting impacts transactions only from the time of the
change. Because past transactions aren’t recalculated based on the updated
currency selection, historical data can appear skewed. For example, if a
profile has a loan-to-value of $100, changing the currency selection to euro
visibly changes the value to €100, but doesn’t convert the dollar value to
euros.

If your site uses more than one currency, Personalization uses the current
exchange rate to convert monetary values for reports and analytics.

  4. If your site supports multiple locales, select **Enable Localization of Catalog Metadata Based on Page Locale** so that Personalization stores metadata separately for each locale.

Personalization formats the language and currency in recommendations using the
customer’s locale. For example, a customer in Italy receives the
recommendations in Italian and the currency is in euros.

  5. Save your work.

#### See Also

  * [Catalog Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object.htm&language=en_US&type=5 "Catalog objects and their relationships define the structure of your catalog. Personalization uses catalog objects to interpret and understand customer engagement and affinities. Examples of catalog objects include products, articles, blog posts, categories, brands, styles, and features. Personalization includes several built-in catalog objects, and you can create custom ones to meet your specific needs.")

