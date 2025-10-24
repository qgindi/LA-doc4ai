# Method `Au.script.isRunning`

## Overload 1

Returns `true` if the specified script task is running.

```
public static bool isRunning(string name)
```

##### Parameters

- *name*  (`string`):
    Script file name (like `"Script43.cs"`) or path in workspace (like `@"\Folder\Script43.cs"`), or full file path.

##### Returns

`bool`

* * *

## Overload 2

Returns `true` if the specified script task is running.

```
public static bool isRunning(int processId)
```

##### Parameters

- *processId*  (`int`):
    Script process id, for example returned by `Au.script.run`.

##### Returns

`bool`

##### Exceptions

- `ArgumentException`:
    *processId* is 0 or id of this process.

#### Remarks

The script process can be started from editor or not.