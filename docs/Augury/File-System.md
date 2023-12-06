# File-System
File system related functions

## `file_directory_get_contents(dirPath, filter, includeDirs?, recursive?)` → *array<string>*
|`dirPath` |string |The path of the directory |
|`filter` |string |File extensions to to get ("*.json;*.png;") |
|`includeDirs?` |bool |Whether or not to include folders in the returned array |
|`recursive?` |bool |Whether or not to recursively loop through all subdirectories and include their content |

## `file_directory_print_contents(dirPath, filter, includeDirs?, recursive?)` → *string*
|`dirPath` |string |The path of the directory |
|`filter` |string |File extensions to to get ("*.json;*.png;") |
|`includeDirs?` |bool |Whether or not to include folders in the returned array |
|`recursive?` |bool |Whether or not to recursively loop through all subdirectories and include their content |

## `file_executable_get_directory()` → *bool*
Returns the file path for the game's executable

## `file_project_get_directory()` → *string*
If the game is ran from the IDE, this will return the file path to the game's project file

## `file_directory_get_appdata_path()` → *string*
Returns the current user's appdata folder path

## `file_directory_exists(directoryName)` → {rv}
Checks to see if the given directory exists or not

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`directoryName` |string |The filepath of the directory to check |

## `file_directory_create(directoryName)` → {rv}
Creates a new directory with the given name

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`directoryName` |string |The filepath of the directory you wish to create |

## `file_get_name_from_path(filePath, includeExtension)` → {rv}
Returns just the file name from the given filepath. Example: "appdata/local/augury/file.txt" --> "file.txt" or "file" depending on the includeExtension argument

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`filePath` |string |The path to the file |
|`includeExtension` |bool |Whether to include the file extension in the returned string |

## `file_get_inner_most_directory(_path)` → {rv}
Returns the inner most directory from the given path. Example: "appdata/local/augury" --> "augury"

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`path` |string |The path including the directories |
