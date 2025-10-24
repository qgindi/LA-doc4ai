# Method `Au.process.getCommandLine`

Gets the command line string used to start the specified process.

```
public static string getCommandLine(int processId, bool removeProgram = false)
```

##### Parameters

- *processId*  (`int`):
    Process id.
- *removeProgram*  (`bool`):
    Remove program path. Return only arguments, or empty string if there is no arguments.

##### Returns

`string`

`null` if failed.

#### Remarks

The string starts with program file path or name, often enclosed in `""`, and may be followed by arguments. Some processes may modify it; then this function gets the modified string. Fails if the specified process is admin and this process isn't. May fail with some system processes. Fails if this is a 32-bit process.