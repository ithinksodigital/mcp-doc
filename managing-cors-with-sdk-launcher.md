# Manage CORS with the Salesforce Interactions SDK Launcher

The Salesforce Interactions SDK Launcher is a Google Chrome extension that
supports launching the Marketing Cloud Personalization Visual Editor on any
domain. You can install this extension from the [Chrome Web
Store](https://chrome.google.com/webstore/detail/salesforce-
interactions-s/mhmpepeohaddbhkhecaldflljggicedf/related).

If you have the legacy Evergage Visual Editor Chrome extension installed, you
must **disable** it for the Salesforce Interactions SDK Launcher to work
correctly.

  * The value of the [`default-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/default-src) directive must include `'https://cdn.evergage.com'`.
  * If you're using [`media-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/media-src), [`script-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src), [`img-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/img-src), or [`style-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/style-src) directives in place of [`default-src`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/default-src), then each directive must include `'https://cdn.evergage.com'` in their values.
  * If the policy includes the [`frame-ancestors`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors) directive, the value must include `'self'`. (Generally, if this directive is in use, its value is set to `none`, which prevents the Visual Editor from framing in your page.)

`X-Frame-Options` must be set to `SAMEORIGIN` which allows the page to be
displayed within an `<iframe>`, provided that the parent/frame domains are of
the same origin.

Some pages utilize other methods of blocking the loading of unknown resources.
If your page restricts the loading of scripts or assets to specific domains in
different ways, you must allowlist `https://cdn.evergage.com`.

To ensure that the Salesforce Interactions SDK Launcher extension works
correctly, check and configure the following extension and browser settings.

  * Access `chrome://extensions` on Google Chrome 
    * Select **Details** on the **Salesforce Interactions SDK Launcher** tile
    * Set **Set Access** to **On all site**
  * Access `chrome://settings/cookies` on Google Chrome 
    * Disable **Block third-party cookies**

  * _Salesforce Developers_ : [Content Security Policies and Personalization JavaScript Beacon Directives](/docs/marketing/personalization/guide/content-security-policies-javascript-beacon-directives.html)
  * _External Link_ : [MDN Web Docs: `Content-Security-Policy`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy)

