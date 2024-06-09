

# About Audience Segments

A segment is a real-time grouping of users or accounts, based on criteria you
define using a set of segment categories and rules. With segments, you can add
another layer of personalization to your campaigns, and gain deeper insight
into your customers. Segments can even include groups you've already defined
in your CRM, DMP, or marketing automation platform.

## Audiences

You can use audiences for analytics and cross-channel campaign targeting. You
can export audiences to use the data in other systems. You can also use
audience membership, when a user or account joins a segment or leaves a
segment, to trigger events in other systems.

The information that the Personalization system collects about your audiences,
along with data from your other systems, is accessible through comprehensive,
visual profiles—the Unified Customer Profile and the Unified Account Profile.

## Segments

Segments are one of the key components of the Personalization system. A
segment is a real-time grouping of users, or accounts, based on criteria you
define using a set of segment categories and rules.

When a user interacts with one of your channels, the Personalization system
identifies the segments they belong to based on real-time session activity.
Because segment updates happen in real time, membership changes occur
immediately. You can analyze segment data in the Personalization system, and
you can export segment data using the segment exporter or as a .csv file. For
more information, see [Export a Segment to the Personalization
SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5
"Set up a nightly feed or a one-time export to synchronize segments with the
Personalization SFTP. You can then use these segments in other systems to
target cross-channel communications. For example, you can synchronize a
segment to Marketing Cloud to target a specific group with an email
communication.").

## How to Work With Segments and Audiences

When a user interacts with one of your channels, the Personalization system
identifies the segments they belong to based on real-time session activity.
Because segment updates happen in real time, membership changes occur
immediately.

When you combine segments with unlimited historical behavior, user profile
details, and situational data (such as location, weather conditions, and
source), you can define even more granular user segments. You can also segment
your audiences based on email or ad campaigns, and use the results to adjust
user experiences accordingly. You can analyze segment data in the
Personalization system, and you can export segment data using the segment
exporter or as a CSV file. For more information, see [Export a Segment to the
Personalization
SFTP](https://help.salesforce.com/s/articleView?id=sf.mc_pers_segment_export_sftp.htm&language=en_US&type=5
"Set up a nightly feed or a one-time export to synchronize segments with the
Personalization SFTP. You can then use these segments in other systems to
target cross-channel communications. For example, you can synchronize a
segment to Marketing Cloud to target a specific group with an email
communication.").

## View Existing Segments

You can view existing segments by selecting **User Segments** | **User Segments** from the main navigation. If your dataset is configured to support accounts, you also have the option to select **User Segments** | **Account Segments**.

## Example of Using Segments

Suppose you’re a retailer who wants to target shoppers with less than $100
worth of products in their shopping carts to encourage them to add more
products. You can create a segment that targets those users, and then
configure your campaign to appear only for users in that segment. Because
segment updates occur in real time, shoppers who accumulate more than $100 in
their carts during the same visit are no longer members of the segment. So,
Marketing Cloud Personalization doesn’t include them in the campaign, and they
don’t see the incentive.

