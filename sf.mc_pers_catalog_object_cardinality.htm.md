

# Category Cardinality Options

Before building your category hierarchy, determine which category cardinality
you want to use: one per item or many per item. You choose the cardinality in
the Category catalog object. The Category catalog object plays a key role in
category assignment and tracking statistics.

Cardinality Option | Is a category present in an item action event? | Actions  
---|---|---  
One per Item | Yes | 

  * The category is set as the item’s category, replacing existing categories. If the event contains more than one category, the first category in the list is used.
  * Statistics are tracked for the new category.

  
No | 

  * No category change occurs.
  * Statistics are tracked for the existing categories.

  
Many per Item (default) | Yes | 

  * The category is added to the item’s set of categories.
  * Statistics are tracked only for the added category.

  
No | 

  * No category change occurs.
  * Statistics aren’t tracked for the existing categories, unless the item contains only one category. For example, in a purchase interaction, if an item has multiple categories, no category revenue attribution occurs because categories can’t be included on purchase line items.

