# Fear System
v1.1
 - 10-3-22: Changed to use DS grids

 

 This system controls an NPC's reaction to other NPCs and objects

 Each NPC has a fear level(an integer), once that fear level passing a certain threshold, the NPC starts to flee.

 An NPC's fear level will primarily increase from other, hostile NPCs being near them



 ?> This system may need to be refactored/reworked in the future


## `npc_fear_system_init()` → `undefined`
inits all variables and data strucs used for the npc fear system

## `npc_fear_add_object(objectIndex, fearAmount)` → `undefined`
Adds an object to the list of objects that this NPC fears, and the amount it fears it,
		  If the object is already in the grid, then the fear values will be added together


| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`objectIndex` |asset.object |The object that the NPC will fear |
|`fearAmount` |real |The amount of the fear the object gives the NPC |

## `npc_fear_get_fear_amount_object(objectIndex)` → *real*
returns how much this NPC fears the given object or -1 if the object_index isn't in the array

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`objectIndex` |id.instance |The object you want to check for |

## `npc_fear_process_main(instance)` → `undefined`
the main loop of the NPC fear system, runs in the npcMasterParent

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`instance` |id.instance |the instance the main loop with be ran in |

## `npc_fear_remove_object(objectIndex)` → `undefined`
removes a given fear amount from the given object if it exists within the grid

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`objectIndex` |asset.object |The object that will be removed from the instance's feared objects |
