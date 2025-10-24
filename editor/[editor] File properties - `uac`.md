# File properties - `uac`

[UAC](../articles/UAC.html) integrity level (IL) of the task process.

- `inherit` (default) - the same as of the editor process (High IL recommended).
- `user` - Medium IL, like most applications. The task cannot automate high IL process windows, write some files, change some settings, etc.
- `admin` - High IL, aka "administrator", "elevated". The task has many rights, but cannot automate some apps through COM, etc.

This property is ignored when the script runs as exe program started not from editor. Then it's an ordinary program.