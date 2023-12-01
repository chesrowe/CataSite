# Unit-Array
Functions that manipulate the unit selection array

## `unit_array_set_move_target(run)` → `undefined`
Sets all selected units to move toward the current mouse position

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`run` |bool |Whether or not the units should run to their new move target |

## `unit_array_set_attack_target(targetId)` → `undefined`
Sets all guardians that are currently selected to attacking the given instanceId

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`targetId` |id.instance | |

## `unit_array_check_for_type(object_index)` → *bool*
Checks the unit array for an instance of a given object index and returns true/false

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`object_index` |asset.object |The object to check for |

**Returns:** Whether or not an instance of the given type was found

## `unit_array_add(unitId)` → `undefined`
Adds a unit to the selection array

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`unitId` |id.instance | |

## `unit_array_clear()` → `undefined`
Deselects all units that are currently selected

## `unit_array_set_resource_target(state,target);` → `undefined`
Sets the selected workers to working on a given resource

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`state` |real |The state to set the unit's to |
|`target` |id.instance |The target(a resource) the unit's will be working on |

## `unit_array_remove_id(unitId)` → `undefined`
removes the given unit id from the array

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`unitId` |id.instance |The instance id of the unit to remove |

## `unit_array_clear_ext(unitType1, [...])` → `undefined`
Deselects all units of the given types

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`unitType` |asset.object | |
|`[...]` |asset.object | |

## `unit_array_execute_method(method)` → `undefined`
Iterates over the unit array and executes a method for each unit

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`method` |function |The method to execute for each selected unit |

## `unit_is_selected(unitId)` → *bool*
Checks to see if a unit is selected by the player

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`unitId` |id.instance |The instance id of the unit that is being checked |

**Returns:** Whether or not the given unit is selected
