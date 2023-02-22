# Inventory

## Item lifecycle

| Status              | Next state                                                                              | Allowed actions                                                                                                                       | Restricted actions                                                                                                                                                        |
| ------------------- | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pending             | <ul><li>Planning</li><li>Active</li><li>Pending obsolescene</li><li>Obsolete</li></ul>  | <ul><li>Insert into storeroom</li> <li>Update reorder details in inventory</li> <li>Update vendor to buy from.</li></ul>              | <ul><li>Add to jobplan.</li> <li>Change current balance.</li> <li>Perform physical count.</li> <li>Set average or standard cost.</li><li>Add to purchase order.</li></ul> |
| Planning            | <ul><li>Pending</li><li>Active</li><li>Pending obsolescene</li><li>Obsolete</li></ul>   | <ul><li>Add to job plan</li> <li>Mark job plan active.</li> <li>Apply job plan to workorder.</li><li>Add to purchase order.</li></ul> | <ul><li>Issue item.</li> <li>Balance adjustments.</li><li>Set average or standard cost.</li><li>Approve PO.</li></ul>                                                     |
| Active              | <ul><li>Pending</li><li>Planning</li><li>Pending obsolescene</li><li>Obsolete</li></ul> | All actions                                                                                                                           | No restrictions                                                                                                                                                           |
| Pending obsolescene | <ul><li>Obsolete</li></ul>                                                              | <ul><li>Issue, return, transfer.</li><li>Receive item for approved PO.</li></ul>                                                      | <ul><li>Approve PO.</li><li>Reorder.</li></ul>                                                                                                                            |
| Obsolete            | None                                                                                    | No longer usable                                                                                                                      |

**Item cannot be marked OBSOLETE, if it exists on**

- Workorder planned material
- Jobplan material
- Purchase requisition
- Purchase order
- Inventory balance
- Asset