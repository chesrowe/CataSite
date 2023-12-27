# Misc serialization functions
Misc serilization functions, idk */

## `json_load(filePath)` → *struct <span style="color: red;"> *or* </span> array <span style="color: red;"> *or* </span> -1*
Loads a json file and parses in as a struct(or array) then returns that struct(or array) or -1 if failed.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`filePath` |string |The path to the json file |

## `json_load_encoded(filePath)` → *struct <span style="color: red;"> *or* </span> array <span style="color: red;"> *or* </span> -1*
Loads a json file that may be base64 encoded and parses in as a struct/array then returns that struct/array or -1 if failed.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`filePath` |string |The path to the encoded json file |

## `grid_to_array(grid)` → *array*

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`grid` |id.ds_grid | |
Converts a ds_grid to a 2D array.

## `array_2d_to_grid(array)` → *id.ds_grid*

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`_array` |Array | |
Converts a 2D array to a ds_grid.
