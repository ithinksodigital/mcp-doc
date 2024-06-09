

# Promotion Management for Einstein Decisions

After you configure Einstein Decisions, add an initial set of promotions and
assets to a dataset, and publish an Einstein Decisions campaign, you can begin
planning your ongoing promotion management.

### Required Editions

Available in: Premium edition  
---  
  
## Promotions in Einstein Decisions

Einstein Decisions uses powerful machine learning to make its assessments. To
maintain a low latency, it analyzes and chooses 50 promotions at a time. You
can have more than 50 promotions in Marketing Cloud Personalization, so use
eligibility rules to keep the number of promotions that a single user is
eligible for below 50. If a user is eligible for more than 50 promotions,
Personalization chooses a random selection of 50 for Einstein Decisions to
evaluate.

The more promotions you include, the more likely there’s a perfect option for
each user. However, the fewer promotions you include, the quicker learning
occurs. Generally speaking, expect 10,000 impressions per promotion before you
start to see lift from Einstein Decisions, depending on your use case.

Einstein Decisions presents promotions, but doesn’t provide the ability to
sort them. So, if you have 10 promotions that you want to sort and display on
a page, don’t use Einstein Decisions. If you want to determine the best five
promotions to show from a set of 10, Einstein Decisions displays the best five
promotions for each individual user.

For the machine learning training to work properly, there must be more
eligible promotions for a decision than the number of decisions that return in
a response. So, if you want an Einstein Decisions campaign to present three
promotions on a homepage, you must have at least four eligible promotions to
choose from for learning to occur. If not, the available promotions still
display, but there’s no learning because all promotions return.

## Metadata and Promotions

Metadata gives the machine learning model hints about similarities between
promotions. For use cases with a small number of promotions, the value is
minimal because the algorithms learn everything they need from user behavior.
In use cases where there are a large number of promotions, or when promotions
are frequently cycled in and out, metadata can help speed up learning.

Attribute metadata lets you specify properties for your promotions. For
example, “discount level” can offer a hint to the machine learning model when
comparing promotions where some are offering discounts. The model training
learns faster because it uses what it learned about previous promotions
offering discounts when determining how to handle new promotions that offer
discounts.

You can safely mix promotions with and without metadata. The machine learning
model learns the promotions with metadata more quickly and can serve them with
greater accuracy, but the promotions without metadata aren’t penalized.

## Content Zones and Tags

When adding promotions and assets to Marketing Cloud Personalization, you must
decide whether to use an existing content zone or tag, or to create a content
zone or tag. When using a content zone or tag in a live campaign, machine
learning begins accumulating data for the assets associated with that content
zone or tag.

If you use the Einstein Decisions global web template for a promotion, the
assets must have a content zone or tag that matches one of the content zones
configured in your site map. The server-side Einstein Decisions template isn’t
limited to content zones mapped in the site map, and can use any content zone
or tag.

## Using an Existing Content Zone or Tag

For promotions with an asset that uses an existing content zone or tag, the
new asset often initially only returns in the 10% of impressions that Einstein
Decisions reserves for exploration and learning. This controlled introduction
occurs because Einstein Decisions needs data about the new asset to determine
its efficacy in comparison to the existing assets.

Because of this approach, you can expect lower numbers of views and clicks for
a new asset after you initially add it. When Einstein Decisions collects
enough data, the new asset returns more frequently, depending upon its
performance. This situation is called the “cold start” problem, and can be
improved by providing appropriate promotion metadata. When a new promotion has
metadata showing its similarity to existing promotions, machine learning can
use those previous learnings to make quicker decisions.

## Creating a Content Zone or Tag

When you create a content zone or tag for an asset, there aren’t any
historical learnings available in the initial campaign. Einstein Decisions
introduces assets with a new content zone or tag randomly to allow for initial
data collection and model learning. The first training begins after 100
decisions. Additionally, expect 10,000 impressions per promotion before you
start to see lift from Einstein Decisions, depending upon your use case. For
example, a use case choosing between homepage heroes targeting different
audiences personalizes more quickly than a campaign that makes similar offers
with slightly different imagery on a small corner of a page.

Consider the following when adding promotions and assets:

  * Does the content zone or tag connect to the purpose of the promotion? If you’re adding a promotion about an ongoing winter sale and you have live promotions with “Winter Sale 2022” as the content zone, reusing that tag makes sense because the promotions have a common initiative. If you’re doing a full window refresh and introducing new promotions to replace an existing set of live promotions, a new tag or content zone is likely the best decision. This strategy allows for a quicker initial learning process by ensuring the new promotions and assets aren’t competing for traffic with existing ones.

  * How do the new promotions and assets map to your campaign strategy? If the new promotions and assets reuse an existing content zone or tag that’s in a live campaign, the new assets are immediately eligible to return to users. If you use a new content zone or tag, you must configure and publish a new campaign targeted to the content zone or tag, or update an existing campaign.

  * If you use a new content zone or tag, are there enough new promotions to allow for proper learning? For learning to occur, there must be at least one more promotion eligible to return than the number that the campaign is configured to return. The Einstein Decisions algorithms can’t learn unless they make decisions. So if all eligible promotions return every time, no decisions are made and no learning occurs.

