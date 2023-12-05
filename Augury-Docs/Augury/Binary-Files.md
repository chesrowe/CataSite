# Binary-Files
Functions for writing to and reading from binary files

## `file_bin_read_real(file);` → *real*
reads a real value from a binary file

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`file` |id.binaryFile |The id of the file to write the data to (File mist be previously opened using `file_bin_open`) |

## `file_bin_read_string(file);` → *string*
Reads a string from a binary file.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`File` |Id.BinaryFile |The file to read the data from |

## `file_bin_read_type(file);` → {rv}
Not sure what this is for, but it was here, so let's document it, literally just calls `file_bin_read_btye`

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`file` |id.binaryFile |The file to write the data to |

## `file_bin_write_real(file, data);` → {rv}
Writes a real value as bytes of data.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`file` |id.binaryFile |The file to write the data to |

## `file_bin_write_string(file, data);` → {rv}
Breaks a string down to individual bytes then writes them to a binary file.

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`file` |Id.BinaryFile |The file to write the data to |
|`data` |string |The string to break down to binary data. |
