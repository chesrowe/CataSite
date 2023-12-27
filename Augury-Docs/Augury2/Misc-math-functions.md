# Misc math functions
Random math functions that may get used frequently or maybe not so. Seems to vary.

## `round_decimals(number, decimalPlaces)` → *real*
Rounds a number to the given amount of decimal places

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`number` |real |The number you want to round |
|`decimalPlaces` |real |The number of decimal places you want to round to |

**Returns:** The rounded number

## `floor_decimals(number, decimalPlaces)` → *real*
Floors a number to the given amount of decimal places

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`number` |real |The number you want to round |
|`decimalPlaces` |real |The number of decimal places you want to floor to |

**Returns:** The floored number

## `ceil_decimals(number, decimalPlaces)` → *real*
Ceils a number to the given amount of decimal places

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`number` |real |The number you want to round |
|`decimalPlaces` |real |The number of decimal places you want to ceil to |

**Returns:** The ceiled number

## `difference(val1,val2)` → *real*
finds the absolute difference between 2 values

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`val1` |real |The minimum value |
|`val2` |real |The maximum value |

## `wrap_value(value,min,max)` → *real*
returns the value wrapped.If it is above or below the threshold it will wrap around

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`value` |real |The value to wrap |
|`min` |real |The minimum vale |
|`max` |real |The maximum value |

## `norm(min, max, value)` → *real*

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`min` |real |The minimum value |
|`max` |real |The maximum value |
|`value` |real |The value to normalize |
Normalizes a value for the given min and max based on the value given

**Returns:** The normalized value

## `lerp_clamped(val1, val2, amount)` → *real*
Performs a lerp but locks the returned value between val1 and 2.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`val1` |real |The minimum value |
|`val2` |real |The maximum value |
|`amount` |real |The amount |

**Returns:** The lerped value

## `value_is_between(val1, val2, checkValue)` → *bool*
checks to see if the checkValue is between val1 and val2 and if so, returns true, else false

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`val1` |real |The minimum value |
|`val2` |real |The maximum value |
|`checkValue` |real |The value to check |

**Returns:** Whether `checkValue` is between `val1` and `val2`

## `seconds_to_frames(numberOfSeconds)` → *real*
Takes a number of seconds and converts it to game frames

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`numberOfSeconds` |real |The number of seconds to convert to frames |

**Returns:** The number or frames

## `map_value(value, currentLowerBound, currentUpperBound, desiredLowerBound, desiredUpperBound)` → `undefined`
map a value from one range to another

## `surface_get_size(surface)` → *real*
Gets the size of a surface in bytes (height * width * 4)

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`surface` |id.surface |The surface to get the size of. |

**Returns:** The size of the given surface in bytes
