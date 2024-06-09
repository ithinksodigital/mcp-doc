

# About Personalization Datasets

Learn more about datasets in Marketing Cloud Personalization.

## What are Personalization Datasets?

A dataset represents an instance of Personalization. User profiles, campaign
configurations, and other features of Personalization are scoped to a dataset.
This scoping strategy enables you to use different datasets for different
sites, geographies, or deployment environments. For example, it's common to
split datasets between your QA and production environments, and it’s also
helpful to maintain separate datasets for your French and German sites.

## Multiple Datasets Per Personalization Account

A Personalization account can have multiple datasets. To learn how many you
can have for your Personalization account, see [Personalization
Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_limits.htm&language=en_US&type=5
"Learn about the limits and capabilities in Marketing Cloud
Personalization.").

## Types of Datasets

Each dataset is configured to be one of the following types:

  * Production
  * Staging
  * QA
  * Development

## Identity Groups

Datasets are placed within identity groups to coordinate user identities
between environments. This method ensures that you don’t email the same user
from both the French and German environments, while still letting each dataset
coordinate that user's personalization.

## Ways to Use Datasets

You can use datasets in various ways. For example:

  * Set up a test dataset to monitor your QA or staging environment, and a production dataset to monitor your live production site. Having another dataset keeps real customer data separate from the data you generate during testing.

  * Separate data from different business units with different customers.

  * Track your website separately from your application.

