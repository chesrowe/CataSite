# Drop tables
Drop tables are meant to have a "primary" drops (like stone dropping.... stone) and more rare secondary drops (like stone rarely dropping a gemstone).
Meaning you always want to add at least one drop to a drop table with a drop chance of 1 (meaning always drops if nothing else does).
Failing to do this will result in the dropTable returning an empty struct (It thinks the table is empty)
This is because the most rare drops are meant to supplement the main drop at no set amounts */
## Example:
```gml
monsterDropTable = new dropTable(10); //Create a new drop table with 10 total items on it
monsterDropTable.dropAdd("itemResourceCreatureHide", 5, 1); //Add an hide drop to the droptable with a 1 in 5 chance of dropping, with 1 dropping each time it is rolled.
var _drop = monsterDropTable.dropRoll(); // Rolls a drop and stores it in `_drop`
```

## `dropTable(maxItemAmount)` (*constructor*)

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`maxItemAmount` |real |The amount of items that the droptable contains, after all the items have been dropped, EMPTY_STRUCT will be returned |
```gml
if (gay){
fuck();
}else if (pan){
fuckAll();
}
