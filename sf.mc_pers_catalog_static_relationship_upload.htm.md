

# Upload Static Relationships

After you define static relationships for your catalog, you can upload a CSV
file to associate products with each other. You can then use static
relationships in an Einstein Recipe so that Personalization can recommend
associated products to your customers.

### Required User Permissions

Permissions Needed  
---  
To upload static relationships: | A role with Catalog Create/Edit permissions  
  
Before you can upload static relationships to associate (or disassociate)
products with each other, you must define the static relationships for your
catalog.

  1. Create a CSV file by entering “items” into cell A1 and, starting at cell A2, the product IDs for each product that you want as an anchor product.
  2. Enter "linkedItems" in cell B1, then enter the product IDs (separated by commas) in the column B cells you want to associate with each product in column A. 

![169e5640-db64-4488-8075-7077f7b81f9a]

![e3d402f5-4239-40fb-9faa-bedfc432aaf2]

Note The product association isn’t bidirectional. For example, if product A is
the anchor product and you associate product B with it, only product B returns
for product A. For product A to also return for product B, you must also
associate product A with product B when product B is the anchor product.

  3. Save the file.
  4. In the **Catalog** section of the main navigation, select **Catalog** | **Products**.
  5. Click **Upload Relationships** in the upper right corner.
  6. In the **Upload New Product Relationship** dialog, select the static relationship you want to use for your file.
  7. If you’re removing a static relationship for the list of products, select **Remove relationships from items**.
  8. Click **Upload Relationships**.
  9. Click **Select files** to locate and select your CSV file, or drag the file within the dotted lines of the dialog.

