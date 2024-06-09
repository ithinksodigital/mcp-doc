

# Campaign Statistics Optimizations by KPI

Every campaign and use case is distinct, with their own nuances. However, when
thinking about how to improve and optimize your campaign performance, these
general guidelines can help.

**Key Performance Indicator (KPI)** |  **What You See in Campaign Statistics** |  **Recommended Optimizations**  
---|---|---  
Click-Through Rate (CTR) | Control is beating the test click-through rate. | Consider changing one of these campaign components.

  * **Messaging** —Make the messaging more engaging.
  * **Look and feel** —Create a more prominent call-to-action.
  * **Recommendations** —Review the recipe for potential optimizations.

  
Conversion Rate | Control is beating the test conversion rate.Note: In many cases, the conversion rate can be the goal-completion rate. | Consider changing one of these campaign components, or consider pausing the campaign and revisiting your hypothesis.

  * **Placement** —Is the campaign distracting the visitor from converting? Consider a different placement in a less distracting location.
  * **Customer journey** —Is the campaign disrupting the customer journey? Consider re-evaluating your hypothesis and changing when the campaign triggers.
  * **Recommendations** —Is the recipe recommending items that are distracting the visitor from their path to conversion? 

  
Average Order Value (AOV) | Control is beating the test average order value. | Consider changing one of these campaign components:

  * **Offers or promotions** —Is the campaign displaying an offer that would lower the total purchase price? Are you seeing a correlated increase in conversion rate?
  * **Recommendations** —Is the campaign recommending lower-priced products? Consider adjusting the recipe, possibly by adding a price inclusion rule.

  
Revenue Per User (RPU) | Control is beating the test revenue per user. | Revenue per user is a combination metric derived from the average order value and conversion rate. If the test experience is losing revenue per user, consider other optimizations listed in this chart. In addition, evaluate whether you selected the optimal audience for your campaign. Consider these examples:

  * First-time purchasers could be turned off by your upsell attempts, while returning customers could be more receptive. Consider limiting the upsell campaign to returning purchasers.
  * A campaign with an offer targeted at frequent visitors could be unnecessary. In fact, you could be training your customers to wait for offers before making a purchase. Consider limiting this type of campaign to new or lapsed visitors.

  
Impression Volume | Impression volume is below expectations. | Review the campaign and experience targeting rules.

  * Is the audience for this campaign too narrow? Consider relaxing the targeting rules.
  * Are the actions or pages targeted by the campaign tracking properly? Test the targeted actions yourself across browsers and devices and in an incognito window, and confirm they’re working properly. For web campaigns, use the [Campaign Debugger](https://developer.salesforce.com/docs/marketing/personalization/guide/campaign-debugger.html) feature in the Salesforce Interactions SDK Launcher Chrome Extension to validate that you see the action tracked.
  * If the campaign targets a page element that loads slowly, it can prevent the campaign from rendering for visitors with poor internet connections. Work with your developer to confirm the web template is built properly and performant.

  
Bounce Rate(track bounce rate using a third-party analytics platform, such as Google Analytics) | The test experience causes a higher bounce rate or shorter visits, without conversion, than control. | Your campaign could be distracting or annoying to your visitors.

  * Review the campaign configuration and rules, and confirm that they’re configured properly. For example, a popup on every page load of a visit could be annoying. A best-sellers recommendations campaign targeting the checkout page could also be annoying or distracting.
  * Review your hypothesis carefully, and determine if the campaign could be annoying or frustrating to your visitors. 
  * Ensure that your campaign loads quickly and, if it's replacing existing content, that it doesn’t flicker. Slow-loading campaigns can frustrate visitors. If your campaign isn’t loading with the rest of the page, work with your developer to improve the template.

  
  
#### See Also

  * [ _Developer Documentation_ : Campaign Debugger](https://developer.salesforce.com/docs/marketing/personalization/guide/campaign-debugger.html)

