# Inventory-Class
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
### `.permittedItemTypesRemove(itemConstructorName)` → `undefined`
Removes an item type

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemconstructorName` |string |The string name of the item's constructor |

### `.resize(size)` → `undefined`
Changes the number of item slots an inventory has

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`size` |real |The new number of item slots |

### `.getSize()` → *real*
Returns how many slots an inventory has

### `.isFull()` → *bool*
Returns whether the inventory is full or not

### `.isEmpty()` → *bool*
Checks to see if there are any items at all in the inventory

### `.percentOfSlotsEmpty()` → *real*
Returns the percentage of the inventory that is empty

### `.getEmptySlotNumber()` → *real*
Returns the number of empty item slots in a given inventory

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`inventory` |struct.inventory |The inventory of which the empty slots will be counted |

### `.itemCanBeHeld(itemType, [quantity])` → *Bool*
Checks to see if an item of a certain quantity can be held in the inventory

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.itemConstructorName |The type of item that you want to add to the given inventory |
|`quantity` |real |The amount of the given item to add to the given inventory |

**Returns:** Returns Whether or not the given intentory can hold ALL of the given items

### `.itemAdd(itemType, [quantity])` → *real*
Adds a new item of the given type and quantity to the inventory.
This will take up as many item slots as needed to add the given quantity.
If there is not enough space in the  inventory, only the amount possible will be added.
Returns the total amount that was actually added to the given inventory

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemConstructorName` |string.item.constructorName |The type of item that you want to add to the given inventory |
|`quantity` |real |The amount of the given item to add to the given inventory |

### `.itemTransfer(itemType, destInv, [quantity])` → *bool*
Transfers items of a given type from this inventory to another.
Returns whether the function was able to transfer ANY items or not

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.constructorName |The item type that you want to transfer |
|`destInventory` |struct.inventory |The inventory that the items will be tranfered to |
|`quantity` |real |The amount of the item type that you want to transfer |

**Returns:** Returns whether the function was able to transfer ANY items or not

### `.itemTransferSlot(slotIndex, destInv, [destSlotIndex], [quantity])` → *bool*
Moves a quantity of an item from this inventory at a specific slot to another inventory,
equipping/unequipping and swapping as nessesary.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`slotIndex` |real |The index of the slot that is being moved |
|`destInventory` |struct.inventory |Where the item is going |
|`quantity` |real |The amount of an item to move |
|`destIndex` |real |The index within the dest inventory that the item will be placed |

**Returns:** Returns whether or not the move could be completed or not.

### `.itemTransferAll(destInv)` → *array<struct>*
Transfers all the items in the inventory to another inventory.
Returns an array of structs with properites: itemName, itemQuantity, and itemIconSprite

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`destInv` |struct.inventory |The inventory that all the items will be placed in |

**Returns:** Returns an array of structs with properites: `itemName`, `itemQuantity`, and `itemIconSprite`

### `.itemGetAmount(itemType)` → *real*
Returns the amount of a given item type within the inventory

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.constructorName |The type of item that you want to get the amount of |

### `.itemGet(itemType)` → *struct.item <span style="color: red;"> *or* </span> -1*
Returns the item struct of the first item found for the given type or -1

### `.itemRemove(itemType, [quantity])` → `undefined`
Removes items of a given type and quantity from the inventory.
Cool thing about this function is that the type of item can be scoped as widely or as narrowly as you want.
For example: .itemRemove("itemResourceWoodcutting", 100, inv) would remove any items of the woodcutting type.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.constructorName |The itemtype you want to remove from the inventory |
|`quantity` |real |The amount of the given itemType that you want to remove |

### `.itemCraft(itemType, [outputInv])` → `undefined`
Crafts a given item using ingredients from the inventory
Optionally puts the resulting item into another inventory

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.itemConstructor |The type of item to craft |
|`outputInventory` |struct.inventory |Optional: The inventory where the crafted item will be placed |

### `.anyItemsInThisInventoryArePresentInAnother(otherInventory)` → *bool*
Checks to see if any items within this inventory are also present in other

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`otherInventory` |struct.inventory |The other inventory to check for items |

### `.itemCanBeCrafted(itemType, inputInventory, outputInventory)` → *bool*
Checks to see if a given item can be crafted.
The conditions that have to be mets are:
- All the items needed to craft the given item are present in the input inventory
- The output inventory actually has enough space to hold the crafted item(s)

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.constructorName |The type of object you want to craft |
|`inputInventory` |struct.inventory |The inventory containing the ingredients to craft the given itemType |
|`outputInventory` |struct.inventory |The inventory that the resulting item will be put in |
