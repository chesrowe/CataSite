# Discord-Logging
Functions related to logging info to Discord channels

the `DISCORD_CHANNELS` enum contains the channels errorLog, warningLog, and debug console

## `discord_log_warning(_warningMessage)` → `undefined`
logs a warning message to the #augury-warning-log channel

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`warningMessage` |string |The message you want to log to the channel |

## `discord_log_console(debugMessage)` → `undefined`
logs a debug message to the #augury-debug-console channel

| Parameter | Datatype  | Purpose |
|-----------|-----------|---------|
|`debugMessage` |string|array<string> |The message/messages you want to log to the channel |
