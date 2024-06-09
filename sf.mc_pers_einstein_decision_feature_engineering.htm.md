

# Feature Engineering in Einstein Decisions

Feature engineering refers to the process of selecting features to use in a
machine learning model. A feature is a data type that the model can observe
and include in its training. To determine which data Einstein Decisions
references, you define the machine learning features on the Feature
Engineering page.

### Required Editions

Available in: Premium edition  
---  
  
## Training Target

A training target is the response that the machine learning training process
observes, and then creates a model to maximize. Training targets include the
following:

Target | Description  
---|---  
**Click** | This event captures when a user clicks the displayed promotion.  
**Conversion** | A conversion event is represented by the purchase action in Marketing Cloud Personalization. Depending upon your implementation, a purchase event can represent a wide variety of actions. For example, a conversion can be a classic ecommerce transaction, or an application submission or resource download. For B2B, a conversion event can map to a webinar signup or account creation. For most retail use cases, conversions are the best training target to use. The conversion target uses a 24-hour attribution window from the time a promotion displays.   
**Goal completion** | Using goal completion as your training target can be useful when the behavior you want to influence isn’t captured well by conversions. For example, your goal can be to optimize the completion of an insurance quote, or the fulfillment of requests to contact a salesperson. For more information, see [Filters and Global Goals](https://help.salesforce.com/s/articleView?id=sf.mc_pers_filter_and_goal.htm&language=en_US&type=5 "Establishing filters and global goals to better monitor the results of specific campaigns and gauge the impact of campaigns against overall business goals.").  
  
Select the training target that is closest to the business value you’re trying
to capture.

Avoid using the click training target if the conversion or goal completion
target is applicable for your use case. Driving more clicks can be satisfying,
but they generally aren’t inherently valuable by themselves. In some cases,
optimizing for click can reduce business value, as with click-bait promotions
that don't offer a good path to conversion and can end up being overselected.

Even if you don’t select clicks as a training target, Einstein Decisions still
records them and learns from them for other training targets. Even though
clicks don’t directly represent true business value, they’re still a valuable
form of direct feedback, and are often more plentiful than conversions or most
goal completions.

You can change your training target anytime, and data that’s already collected
updates to use the new training target, so nothing is lost. However, if you
change the training target, it impacts all campaigns that are using Einstein
Decisions for next-best-offer decisioning. It can take up to a day before a
change in the training target takes effect.

## Features

Einstein Decisions creates a machine learning model from rows of training
data, where each row contains several columns. Each of these columns is called
a “feature” and is a piece of information that the algorithms can use to make
better decisions.

Generally, a good feature is any piece of information you think is relevant to
the training target or the promotions. For example, if you have promotions for
winter apparel, including a feature about a user's location helps ensure you
don’t promote parkas to users in Florida.

You can include features even if they aren't useful for personalization
because they help identify users that are likely to reach the training target
regardless of what the algorithms do. An example is lifetime value. Generally,
a user who has purchased before is more likely to purchase again, and this
feature helps the machine learning model understand when its decisions make an
impact.

Einstein Decisions includes algorithms that account for irrelevant data so
that it learns to ignore features that aren’t useful. Although it doesn’t add
value to include features that you know are irrelevant, doing so doesn’t
impact the performance of the machine learning model.

Salesforce recommends including all of the default features, as well as any
custom attributes, segment memberships, and catalog objects that you think are
relevant. For the maximum number of features you can specify, see [Einstein
Decisions
Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_einstein_decision_limits.htm&language=en_US&type=5
"Marketing Cloud Personalization has limits for some Einstein Decisions
features.").

