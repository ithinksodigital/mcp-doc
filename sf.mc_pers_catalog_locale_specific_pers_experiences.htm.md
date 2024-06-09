

# Providing Locale-Specific Personalized Experiences

You can deliver locale-specific personalized experiences using webSDK,
triggered email through Marketing Cloud Engagement, or headless APIs.

How Personalization serves locale-specific experiences depends on a number of
factors.

  * The localized experience presented to a consumer is based on the consumer’s locale. The locale is defined on the inbound event through the webSDK or Event API. You must enable catalog localization and ensure that inbound events include the appropriate locale value.
  * If a consumer’s locale doesn’t match the locale of any items in the dataset, Personalization doesn’t return recommendations.
  * If an incoming event doesn't include a locale value, Personalization uses the last locale value stored in the consumer’s profile.
  * If a consumer’s profile doesn’t include a locale value, Personalization uses the dataset’s default locale.
  * Open Time Email supports personalizations only for the default locale. It doesn’t return content based on a consumer’s locale.
  * You can’t set a consumer’s locale using Mobile SDK. When making personalization decisions:

    * If the consumer doesn’t have a locale value, Personalization makes decisions using the locale of the default dataset.
    * If the consumer has a locale value from a prior internet or API event, Personalization makes decisions using that locale.

