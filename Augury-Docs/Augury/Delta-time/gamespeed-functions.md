# Delta time/gamespeed functions
Functions related to Delta time and gamespeed.
Delta time works as a multiplier so the target should be 1 for normal speed.

## `adjust_full(value)` → *real*
returns Multiplies a value by both the Delta time and gamespeed multipliers

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`value` |real |The value to adjust |

**Returns:** The adjusted value

## `adjust_for_delta_time(value)` → *real*
Multiplies a value by the global Delta time multiplier

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`value` |real |The value to adjust |

**Returns:** The adjusted value

## `adjust_for_gamespeed(value)` → *real*
This function multiplies a value by the gamespeed

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`value` |real |a value to be adjusted by the gamespeed |

**Returns:** The adjusted value
