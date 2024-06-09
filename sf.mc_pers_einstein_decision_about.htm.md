

# About Einstein Decisions

Einstein Decisions automates the process of deciding who sees what content, so
you don’t have to manually create complex rules. For example, you define an
area on the homepage for five different promotions—credit cards, mortgages,
auto loans, checking accounts, and retirement plans—and you're not sure which
promotion to display when. Einstein Decisions takes away the guesswork by
continuously learning from the data Personalization collects about users, and
presents the promotion with the highest likelihood of generating the most
lift.

### Required Editions

Available in: Premium edition  
---  
  
## Making Decisions

By evaluating the chance of completion, and the business value of the
promotion to the company, Einstein Decisions determines which promotions to
show to a user to achieve the highest expected value. Einstein Decisions is an
example of a contextual bandit algorithm.

Although you can use prioritization and eligibility rules with Einstein
Decisions, the number and complexity of rules can be reduced when determining
the most relevant promotion for a user. Einstein Decisions uses its machine
learning capabilities to achieve optimal results by:

  * Factoring in extensive data—Einstein Decisions factors in an expansive set of data during its decisioning process. Although it’s always helpful to have as much information as possible about a particular user, Einstein Decisions functions effectively even when there’s little data available. In addition to affinities and intent, which can be unknown for a first-time user, the algorithms also consider information like time of day and day of the week. Additional factors include user-specific data, such as referring source, device type, browser, geolocation, and time since last visit.

  * Being complementary to recommendations—Decisioning is complementary to, rather than a replacement for, Einstein-powered recommendations. Recommendations focus on driving engagement and discovery by presenting products, content, or other catalog aspects, such as brands, categories, and styles, based on a user’s affinities. Einstein Decisions determines the optimal experience to show to a user based on individual data and the business value to your company.

  * Having a simple workflow—You add your promotions and their associated assets, assign content zones and tags to the assets, and include any necessary eligibility rules. Einstein Decisions uses continuous learning to calculate and present the best experience to each user.

## Learning from Experience

Einstein Decisions learns through experience using a constant cycle of showing
a promotion, observing any result, and updating its models to reflect that
observation. Unlike recommendations, which find the most relevant product or
item for a user, Einstein Decisions identifies the promotion that’s most
likely to obtain the desired result based on your training target.

An Einstein Decisions implementation initially returns random results until it
completes its first training, which occurs after 100 decisions. Adding new
promotions to an existing implementation occurs immediately, especially when
using metadata.

To ensure robust learning, Einstein Decisions sometimes returns a random
result. This essential design is known as exploration-exploitation tradeoff,
and is a defining characteristic of contextual bandits. If there’s no feedback
for the training target, learning can’t occur and results continue to be
random. For example, if you set the training target to a completion goal, but
no user ever completes that goal, Einstein Decisions isn’t able to learn.

When Einstein Decisions returns a promotion, it does so by making a
prediction. The machine learning algorithms determine the likelihood for each
promotion to cause the desired outcome, and then returns the promotions with
the highest likelihood.

