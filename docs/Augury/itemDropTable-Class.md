# itemDropTable-Class

## `dropTable(maxItemAmount)` (*constructor*)
|`maxItemAmount` |real |The amount of items that the droptable contains, after all the items have been dropped, EMPTY_STRUCT will be returned |

**Methods**

### `.getItemAmountLeft()` → *real*
Returns the number of remaining items in the drop table

### `.getDrops()` → *array<drops>*
Returns the __drop array

### `.dropAdd(itemConstructorName, dropChance, dropAmount)` → `undefined`

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`itemConstructorName` |string |The name of the item |
|`dropChance` |real |The chance that the item will be dropped when rolling a drop ex: 128 = 1 in 128 |
|`dropAmount` |real |The item quantity that will be dropped if this item is rolled |

### `.dropRoll()` → *struct*
Rolls a drop from the table.

**Returns:** A struct with properties: `itemConstructorName` and `dropAmount`
