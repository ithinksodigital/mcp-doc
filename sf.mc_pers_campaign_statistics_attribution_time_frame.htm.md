

# Attribution Time Frame Explained in Campaign Statistics

Personalization attributes your visitors’ purchase goal completions based on
their interaction, and their level of interaction, with Personalization
campaigns.

Personalization attribution considers only things inside the time frame you
select. Purchases, click-throughs, conversions, and impressions outside of the
specified time frame aren’t considered. Both the Impressed Visit (IV) and the
goal completion or purchase must happen within the time frame that you select.

## Example

Suppose three people visit a website over the course of 2 days. On Day 1, only
Visitors 1 and 2 come to the site. Visitor 1 has an impressed visit and makes
a purchase. Visitor 2 has an impressed visit (IV) but leaves without
purchasing. On Day 2, Visitor 1 has an IV and a purchase. Visitor 2 has two
purchases but doesn’t have an IV. Visitor 3 has one purchase but doesn’t have
an IV. The table summarizes the scenario.

If you select Day 1 as the time frame, Campaign Statistics shows Visitor 1’s
attributed purchase because there’s a campaign impression and a conversion in
the selected time frame.

If you select Day 2 as the time frame, Campaign Statistics shows Visitor 1’s
attributed purchase that occurred on Day 2. The other purchases didn’t happen
after impressed visits during the selected time frame, so they aren’t
attributed to the campaign.

If you include both days in the time frame, Campaign Statistics shows three
attributed purchases: two for Visitor 1 and one for Visitor 2. It’s important
to note that Visitor 2’s on Day 2 doesn’t count towards the conversion rate.
Personalization only counts purchases that follow an impressed visit towards
the conversion rate. Personalization didn’t record an impression for Visitor 3
during the selected time frame, so their purchase isn’t attributed to the
campaign.

| Day 1 | Day 2  
---|---|---  
Visitor 1 | IV - > Purchase |  IV -> Purchase  
Visitor 2 | IV |  \- > Purchase -> Purchase  
Visitor 3 |  | Purchase

