# String Functions
Additional functions that manipulate strings

## `string_has_letters(string)` → *bool*
Checks to see if a given string contains letters or not

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`string` |string | |

## `string_remove_substrings(originalString, substrings)` → *string*
Removes any number of substring(as an array) from the given string

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`originalString` |string |The string from which to remove substrings. |
|`substrings` |array<string> |An array of substrings to remove from the original string. |

**Returns:** The original string with the specified substrings removed.
