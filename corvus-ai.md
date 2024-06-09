# Corvus AI

The Corvus AI is a service responsible for training the Contextual Bandit
leveraged in Einstein Decisions. That service is made available through the
Corvus gear, which allows the fetching of Contextual Bandit arms from within
the context of a campaign template.

Import `ContextualBanditConfig` into any template and define a configuration,
declaring the content zone, maximum number of promotions returned (up to 12),
and explicit fallback promotions to use. Optionally, include a filter on which
promotions are eligible for the bandit.

Import the `decide` function to be used to request contextual bandit
promotions from within the template's `run` method in the server-side
TypeScript. The `decide` function adheres to the following type signature.

The following is an example template that leverages `ContextualBanditConfig`.

To properly train the contextual bandit, it is essential to ensure click log
generation. The Einstein Decisions global web template automatically tracks
click logs and view logs in web campaigns. However, only view logs are tracked
automatically in server-side Einstein Decisions campaigns, while clicks
require manual tracking.

For instructions on ensuring clicks are correctly tracked, refer to the
[Einstein Decisions - Server-Side
Template](/docs/marketing/personalization/guide/einstein-decisions-server-
side-template.html#tracking-click-logs) documentation.

