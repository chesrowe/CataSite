# Inventories
Inventories are data objects used for all instances where we need to store items together
 (Structure storage, pack oxen, unit inventories, and etc..)



 **Examples:**

 ```gml

 toolInv = new inventory(4, ["itemTool"], false)

 storage = new inventory(64, ["item"], true) */

 ```


## `inventory(size, permittedItemTypes, isStorage?)` (*constructor*)
Inventories hold items, have only certain permitted items allowed in them, and can be a storage or "carried"

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`size` |real |The number of item slots the inventory will have |
|`permittedItemTypes` |array<string.item.constructorName> |An array of itemTypes have will be allowed into the inventory |
|`isStorage?` |bool |Whether or not the inventory should hold the maxStorageQuantity or the maxCarryQuantity of an item |

**Methods**
### `.itemTransferAll(destInv)` → *array<struct>*
Transfers all the items in the inventory to another inventory.
       Returns an array of structs with properites: itemName, itemQuantity, and itemIconSprite


| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`destInv` |struct.inventory |The inventory that all the items will be placed in |

**Returns:** Returns an array of structs with properites: `itemName`, `itemQuantity`, and `itemIconSprite`
