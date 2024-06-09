# Recommendations

Marketing Cloud Personalization Recommendations uses a default gear to fetch
recommendations based on the current user and selected recipe. Ultimately, the
Recommendations service supplies all recommendations provided to the
applicable gear component contexts in gears.

The Recommendations gear enables you to configure a campaign template to
control what a business user can configure to drive recommendations for the
template.

To use and configure the Recommendations gear in a campaign template, do the
following.

  1. Add `import { RecommendationsConfig, recommend } from "recs";` to your template's server-side TypeScript. Optionally, to only return item IDs instead of full items, import `recommendIdsOnly` instead of `recommend`.

  2. Add a `RecommendationsConfig` property to your template, and determine what to restrict from the business user, if anything.

     * No restrictions:

     * Restrict business users to be able to recommend only a specific type of catalog items:

     * Restrict business users to a specific maximum number of recommendations:

     * Restrict business users to both a specific type of catalog item and a specific maximum number of recommendations:

     * Restrict business users to a specific type of catalog item and programmatically override an on-page anchor that is used by the recipe:

  3. Use the `recommend` function to use the configuration property of type `RecommendationsConfig` you added.

The following example depicts the usage of the Recommendations gear in a
campaign template.

You can also use the `recommendIdsOnly` function to return only the Item IDs
in order of relevance, as shown in the following example.

The following example shows the `overrideOnPageAnchor` method using a Product
from a Triggered Campaign context as an on-page anchor for the recipe.

If a dataset has locales configured, the Recommendations gear returns items
specific to the user's locale. If a user doesn’t have a locale preference, it
returns items specific to the dataset's default locale. Any item returned from
the Recommendations API is translated into the user's language, provided a
locale item specific to that language exists.

