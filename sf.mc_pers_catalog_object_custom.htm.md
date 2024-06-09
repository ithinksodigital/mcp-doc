

# Create a Custom Catalog Object

Personalization collects behavioral data in the context of the catalog that
you create and uses catalog objects to assess and analyze customer engagement
and affinities. You can add more detail to your catalog by using custom
objects. The more detailed you make your catalog, the more granular your
insights are regarding customer engagement and affinity.

### Required User Permissions

Permissions Needed  
---  
To create a custom catalog object: | A role with Configure permissions  
  
When creating a custom catalog objects, keep these considerations in mind.

  * You can create up to 20 custom catalog objects.
  * Personalization uses the catalog object name in the sitemap, and for ETL data storage and updates.
  * You can’t change the **Name** value after you save the catalog object.
  * Catalog objects and user profile objects can’t have the same name.
  * For a catalog object to appear as one of the four object types in the Affinities graph, assign the Style, Brand, or ItemClass object type as the custom catalog object **Name** value.

To create a custom object:

  1. From the main navigation, select **Settings** | **Catalog and Profile Objects**.
  2. Next to Catalog Object Types, click **+**.
  3. Enter a name for the catalog object up to 30 letters and starting with a capital letter.
  4. For **Label** , enter the text that you want users to see when representing the catalog object in the Personalization application. The label doesn’t affect data capture or storage.
  5. (Optional) For **Description** , describe the catalog object and its purpose.

If your description is more than 200 characters, Personalization truncates the
text and adds an ellipsis (...).

  6. (Optional) Add an attribute to the catalog object.
    1. In the Attributes section, click **New Attribute** and enter a name and label.
    2. Select the attribute type.
    3. Click the checkmark (![68a38d0e-e1f2-4506-82b5-0e4bb43336f0]).
  7. (Optional) Associate an existing custom catalog object with the new catalog object.

![7cb72632-e0cf-4286-8f7d-38cfc6939fd1]

Note Associating a built-in catalog object with a custom catalog object is not
supported.

    1. In the Related Catalog Objects section, click **Add Related Catalog Object**.
    2. In the Related Catalog Object column, select the object.
    3. In the Relationship Cardinality column, select the relationship cardinality.

Item | Description  
---|---  
One per Object | 
       * If an item action event includes the relatedCatalogObject type, Personalization sets the catalog objects for that type on the item, replacing any existing catalog objects for that type. If there’s more than one object type in the event, Personalization uses only the first in the list, and also tracks statistics for the catalog object.
       * If an item action event doesn’t include the relatedCatalogObject type, Personalization tracks statistics for an existing catalog object of that type if one exists for the item.  
Many per Object | 
       * If an item action event includes the relatedCatalogObject type, Personalization adds it to the item's set of catalog objects. Personalization also tracks statistics for all the catalog objects for that type associated with the item.
       * If an item action event doesn’t include the relatedCatalogObject, Personalization tracks statistics for all existing catalog objects of that type associated with the item.  
  
    4. Confirm your selections in the Output/Preview column, and then click the checkmark (![404d65f0-4260-4259-8c69-1f3544673677]).
    5. In the upper-right corner of the Catalog and Profile Objects page, switch the object state to **Enabled**.
    6. Click **Save**.
  8. In Personalization main navigation, click **Catalog** and select the catalog object that you created.
  9. In the upper-right corner of the object page, click **New <Catalog Object>**.
  10. Define attributes and other settings for the catalog object.
  11. Save your work.

#### See Also

  * [Built-In Catalog Objects](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_built_in.htm&language=en_US&type=5 "Built-in catalog objects enable you to quickly begin building your catalog and define its structure. Personalization uses catalog objects to interpret and understand customer engagement and affinities. Personalization collects behavioral data about your customers in the context of your catalog. Catalog objects can be standalone entities, or they can relate to one another to provide a more granular structure for your catalog.")
  * [Customizing the Affinities Graph](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_affinities_graph.htm&language=en_US&type=5 "The Affinities graph displays affinities for objects that use a specific catalog object type as their Name value. You can define custom catalog objects to appear in the Affinities graph when viewing a unified customer profile.")
  * [Catalog Object Limits](https://help.salesforce.com/s/articleView?id=sf.mc_pers_catalog_object_limits.htm&language=en_US&type=5 "Marketing Cloud Personalization imposes limits per dataset for catalog objects and attributes.")

