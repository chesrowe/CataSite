# Item-System-Functions
Functions related to the item system

## `item_exists(itemType)` → *bool*
Checks to see if the given item actually exists or not

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.constructorName |The item that you want to know exists |

## `item_get_struct(itemType)` → *struct.item <span style="color: red;"> *or* </span> -1*
Returns the item struct from global.itemArray for the given or -1 if it can't be found

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemType` |string.item.constructorName |The item that you want to get |
