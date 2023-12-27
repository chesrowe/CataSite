# Array Functions
Functions that manipulate arrays

## `array_add(array, replaceVal, newVal)` → `undefined`
Finds the first index of a 1D array containing an inputed value and replaces in with another value

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`array` |array |The variable containing the array you are adding to |
|`replaceVal` |any |The values in the array that are considered "empty" |
|`newVal` |any |The value that will replace the first "empty" index of the array |

## `array_remove(array, removeVal, emptyVal, [sort?])` → `undefined`
Finds inputed value in the array and replaces it with an empty value, then "sorts" the array.
Sort means moving all the "empty" values to the end of the array so the non-empty values are all at the front
Returns whether or not the removeVal was found

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`array` |array |The variable containing array you want to remove from the given array |
|`removeVal` |any |The value in the array that you want to remove |
|`emptyVal` |any |The value that is considered "empty" within the given array |
|`sort` |bool |Optional: Whether or not to "sort" the array once the value is removed |

## `array_find_number_of_dimensions(array)` → *real*
Finds the number of dimensions an array has

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`array` |array |You know what an array is |

## `array_sort_1d(valToSortOut,array)` → `undefined`
Sorts a given value out of an array leaving no gaps

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`valToSortOut` |any |All of these values will be moved to the end of the array |
|`array` |array |The array to "sort" |

## `array_create_2d(d1Size, d2Size, initValue)` → *array*
Creates a 2D array with the given height and width, each index is given a value

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`d1Size` |real |Size of first dimension |
|`d2Size` |real |Size of second dimension |
|`initValue` |any |The value that will be put in every index |

## `forEachExt(array, function)` → `undefined`
Iterates over an array, executing a given function, whose arguments are the array and the index

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`Array` |array |The array to iterate over |
|`Function` |function |The function to apply to each value in the given array. Func must take 2 arguments array and index |
