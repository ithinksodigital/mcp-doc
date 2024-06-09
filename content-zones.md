# Content Zones

Content Zones are areas throughout a website that you can define to render
Personalization campaigns. The web and server-side campaign templates that you
create using the Personalization UI reference these Content Zones within
campaigns. You can define Content Zones globally in the `globalConfig` or for
a specific page type in the `pageType` configuration.

The following table summarizes the fields that a Content Zone accepts.

Field Name| Expected Value Type| Required| Description  
---|---|---|---  
`name`| String| **Yes**|  The name of the Content Zone. Example:
`global_popup`, `product_detail_recommendations`  
`selector`| String| No| The CSS selector for the Content Zone target  
  
`name` is a required field for all Content Zones, while `selector` is
optional. A Content Zone without a selector is still available to use in
templates that target the glass pane, such as a popup.

Depending on the type of website, certain Content Zones are recommended to be
defined over others to use specific global templates.

The following table outlines Content Zones that enable you to use specific
global templates without additional content zone configuration if mapped via
the sitemap.

Content Zone| Global Template| Description  
---|---|---  
`home_hero`| Banner with Call-to-Action| Content Zone for a hero banner on the
home page  
`home_recs`| Einstein Content Recommendations| Content Zone for
recommendations on home page  
`product_detail_recs_row_1`| Einstein Product Recommendations| Content Zone
for recommendations on a `product_detail` page  
`product_detail_recs_row_2`| Einstein Product Recommendations| Content Zone
for recommendations on a `product_detail` page  
`category_recs`| Einstein Product Recommendations| Content Zone for
recommendations on a category page  
`cart_recs_row_1`| Einstein Product Recommendations| Content Zone for
recommendations on the cart page  
`cart_recs_row_2`| Einstein Product Recommendations| Content Zone for
recommendations on the cart page  
`search_recs`| Einstein Content Recommendations, Einstein Product
Recommendations| Content Zone for recommendations on the search page  
`order_confirmation_recs_row_1`| Einstein Product Recommendations| Content
Zone for recommendations on the order confirmation page  
`order_confirmation_recs_row_2`| Einstein Product Recommendations| Content
Zone for recommendations on the order confirmation page  
`error_page_recs`| Einstein Product Recommendations| Content Zone for
recommendations on an error page  
`add_to_cart_modal_recs`| Einstein Product Recommendations| Content Zone for
recommendations on an Add to Cart Modal  
`global_popup`| Exit Intent Pop-up with Email Capture, Exit Intent Pop-up|
Content Zone for a global popup  
`global_infobar_top_of_page`| Infobar With Call-To-Action, Infobar With User
Attribute and Call-To-Action| Content Zone for an info bar at the top of the
page  
`global_infobar_bottom_of_page`| Infobar With Call-To-Action, Infobar With
User Attribute and Call-To-Action| Content Zone for an info bar at the bottom
of the page  
`global_slide_in`| Slide-In with Call-To-Action| Content Zone for slide-in
messages with call-to-action

