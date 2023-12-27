# keybind system
Augury's keybind system, which is based around keybind "contexts".
A keybind context is a grouping of `keybind` struct. one KBContext is set at any given time.

For example for might be a KBContext for normal gameplay, one for the pause menu, one for when a structure's UI is open, etc

### Enums

### KEYBIND_MODE
The type of check
- direct
- pressed
- released

### KEY CODE
Commonly used keycodes

- period
- comma
- tilde


## `keybindContext()` (*constructor*)
Constructs a new context

**Methods**
### `.keybindAdd(keybind)` → `undefined`
Adds a previously constructed keybind to the context

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`keybind` |struct.keybind |The keybind to add to the context |

## `keybind(key, type, mode, callback)` (*constructor*)
Constructs a new keybind

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`key` |string|real.keycode |Either the keycode or a string like "W" |
|`type` |real.Enum |Either `KEYBIND_TYPE.mouse` or `.keyboard` |
|`callback` |function |A function/method to execute when a keybind is triggered |

**Methods**
### `.rebind(key, type, callback)` → `undefined`
Rebinds the keybind

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`key` |string|real.keycode |Either the keycode or a string like "w" |
|`type` |real.enum |Either `KEYBIND_TYPE.mouse` or `.keyboard` |
|`callback` |function |A function/method to execute when the keybind is triggered |

## `keybind_main()` → `undefined`
The main loop of the keybind system, runs in the controller object
