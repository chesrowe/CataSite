# Markdown-functions
Functions related to generating markdown text

## `array_to_markdown(array, [quotes], [outputFunction])` → *string*

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`array` |array |The array to convert |
|`quotes` |bool |Whether to include quote symbols in the output. Default is false |
|`outputFunction` |function |An optional function to |

**Returns:** A string representation of the array as a Markdown list

## `struct_to_markdown(struct)` → *string <span style="color: red;"> *or* </span> array<string>*
Formats a struct in a pretty-printed JSON code block

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`struct` |struct|array |The struct/array to format |
