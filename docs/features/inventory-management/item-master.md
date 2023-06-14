# Item master

You use the Item Master application to define items that are stocked in your storerooms. You group these items in an item set that can be shared by the organizations that use the item set.

An item has properties like
- Commodity codes
- Order and issue units
- Meter groups and meters
- Type (rotating, condition-enabled, lotted)

Further, other item related functionality includes ability to 
- Associate items with vendors
- Add specifications
- Create item structures
- Create condition-enabled structures
- Create item kits, and add alternate items
- Change the status of the item
- Duplicate the item
- Specify organization details
- Delete items

## Replaceable items (Rotating items)
A replaceable item is an asset such as pump, that you define with a common item number. You designate an item as replaceable because it shares properties of both items and assets.

- It can have an inventory value and an issue cost
- It is an inventory item with a generic item number, a current balance, and multiple instances that can be used in various locations around a plant. (e.g. you might track 10 individual five-horsepower pumps with the single item identifier PUMP-5HP).
- It cannot be consumed, and is maintained as an asset.
- It can only be used in 2 ways
    - Create asset record for tracking
    - Create purchase order for procuring it.
- It is tracked both by its item number in Inventory records and by its asset number in Assets records. 
- It cannot be both a spare part and a replaceable item.

