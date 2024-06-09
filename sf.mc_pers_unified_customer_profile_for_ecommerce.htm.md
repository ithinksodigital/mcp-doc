

# Unified Customer Profile for Ecommerce

The Unified Customer Profile provides an overview of the information that
Personalization collects about a particular user. The information that is
shown depends on the type of business you select (ecommerce).

When you have your site set up to display the Unified Customer Profile for an
ecommerce business, Personalization displays the following information.

## User Snapshot

The user snapshot section at the top of the Unified Customer Profile gives a
quick overview of the user that includes:

Item | Description  
---|---  
User’s name | The unique identifier for a user—a user, ID, email address, person’s name, or a generic label for an anonymous user.  
Average Order Value (AOV) | The average value of the user’s orders for all time.  
Orders | The total number of orders for the user for all time.  
Lifetime Value (LTV) | The total purchase amount for the user for all time.  
Gender Affinity by Purchases | An assigned gender indicator based on what the user shopped for the most.  
Location | The town or city; state, province, or region; and country for the user.  
  
## Affinities Graph

The Affinities graph at the top of the Unified Customer Profile provides a
visual representation of the user’s preferences for various types and
associated catalog items. The circle displays four color-coded types, for
example, brand, style, category, and features. To view a user’s affinity for
any of the types, you can hover over it. Around the outside of the Affinities
graph, up to four of the top items for each type appear with corresponding
color-coded bars that indicate the percentage or amount for each item.

![c4f31ded-1aa9-4067-82e3-efc90ab5e455]

Note You can customize the Affinities graph by assigning the Style, Brand, or
ItemClass object type as the custom catalog object **Name** value. When
configuring a custom catalog object for use with the Affinities graph, the
object **Label** value becomes the screen value.

The affinities graph offers these viewing options.

Item | Description  
---|---  
By Purchases | Clicking the dollar sign icon displays the items and types according to the user’s purchase history. You can hover over an item to see how many times the user purchased it.  
By View Time | Clicking the clock icon displays the items and types according to the user’s view time history. You can hover over an item to see the view duration.  
By Views | Clicking the eye icon displays the items and types according to the user’s view history. You can hover over an item to see how many times the user viewed it.  
  
For example, if a user looks at Brand A products more than any other brand,
the affinities graph shows a higher affinity to Brand A when you select the By
Views option. However, if the same user purchases Brand B products more than
any other brand, the affinities graph shows a higher affinity to Brand B when
you select the By Purchases option.

## Visit History

The time line in the middle of the Unified Customer Profile displays the
user’s visits to your website for all time. You can hover over a visit to view
its date and duration, and any purchases the user made during the visit.

Visits without a purchase are gray, and visits with a purchase are green.
Hovering over a visit adds an orange highlight. Multiple visits on the same
day overlap. You can drag across the time line to zoom in on a particular
period. Clicking **All Time Visits** returns you to the zoomed out view.

## Detail Tabs

The tabs at the bottom of the Unified Customer Profile provide additional
details about the user, including:

Tab | Description  
---|---  
Overview | Includes user details, such as the user ID, username, email address, lifetime value, and last visit, and any identity attributes or other associated attributes. The viewed items stream appears on the Overview tab, and lists all items the user viewed during the indicated period, starting with the most recent. If the user viewed the same item on multiple days, it appears multiple times in the stream.  
Affinity Details | Lists affinities by selected item type along with a streamgraph that shows a visual representation of the selected affinity. You can select an entry in the list to see it visually represented on the graph.  
Event Stream | Lists all actions and visited URLs, and the date of each. Selecting an entry provides more details.  
Action Details | Lists the user’s tracked actions for your site.  
Segment Compare | Provides details about the user when compared across your site and with any segments you add from the **Select a segment** dropdown. You can toggle between data **Averages** and **Totals** for the user.  
Segment Membership | Lists the segments the user is a member of.  
Profile Objects | Displays a table of all configured profile objects and their associated metadata including attributes and related catalog objects. Each tab of the table corresponds to a single profile object. If a profile object has an association with a related catalog object, that value appears as a hyperlink in the table so you can navigate to it.  
  
#### See Also

  * [Customizing the Affinities Graph](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_affinities_graph.htm&language=en_US&type=5 "The Affinities graph displays affinities for objects that use a specific catalog object type as their Name value. You can define custom catalog objects to appear in the Affinities graph when viewing a unified customer profile.")
  * [Unified Customer Profile for Demand Generation](https://help.salesforce.com/s/articleView?id=sf.mc_pers_unified_customer_profile_for_demand_generation.htm&language=en_US&type=5 "The Unified Customer Profile provides an overview of the information that Personalization collects about a particular user. The information that is shown depends on the type of business you select \(demand generation\).")

