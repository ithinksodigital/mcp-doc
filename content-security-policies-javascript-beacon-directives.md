# Content Security Policies and Personalization JavaScript Beacon Directives

The Personalization JavaScript beacon currently uses the [`unsafe-
eval`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-
Security-Policy#unsafe_keyword_values) directive, which allows the use of
dynamic code evaluation functions such as `eval()`. As part of our ongoing
efforts to enhance security standards, we're working on removing the
dependency on `unsafe-eval` in the JavaScript beacon.

In the meantime, if your organization's security scanner flags the presence of
the `unsafe-eval` directive in the JavaScript beacon, include the [`unsafe-
inline`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-
Security-Policy#unsafe_keyword_values) directive in your [Content Security
Policy](/docs/marketing/personalization/guide/managing-cors-with-sdk-
launcher.html##content-security-policy) as a workaround.

Add the [`unsafe-inline`](https://developer.mozilla.org/en-
US/docs/Web/HTTP/Headers/Content-Security-Policy#unsafe_keyword_values)
directive to your Content Security Policy, especially if:

  * your site has a pre-existing Content Security Policy
  * you're using web templates and have the Handlebars Gear enabled
  * you haven't already included the `unsafe-inline` directive in your Content Security Policy.

  * If you're already using `unsafe-eval` elsewhere, you don't have to immediately stop using it. However, you must include the `unsafe-inline` directive in your Content Security Policy. If your Content Security Policy does not currently have `unsafe-eval` but includes `unsafe-inline`, you should not encounter any issues.
  * The changes we're making to the JavaScript beacon are designed with backward compatibility in mind. This approach ensures that you have ample time for conducting security reviews and obtaining necessary approvals before making adjustments to your Content Security Policy.

  * _Salesforce Developers_ : [Managing CORS with the Salesforce Interactions SDK Launcher](/docs/marketing/personalization/guide/managing-cors-with-sdk-launcher.html)
  * _Salesforce Developers_ : [Web Template Handlebars](/docs/marketing/personalization/guide/web-template-handlebars.html)
  * _External Link_ : [MDN Web Docs: `Content-Security-Policy`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)

