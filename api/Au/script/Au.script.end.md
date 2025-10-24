# Method `Au.script.end`

## Overload 1

Ends this process.

```
public static void end()
```

#### Remarks

Calls `System.Environment.Exit`.

It executes process exit event handlers. Does not execute `finally` code blocks. Does not execute GC.

* * *

## Overload 2

Ends another script process.

```
public static bool? end(int processId)
```

##### Parameters

- *processId*  (`int`):
    Script process id, for example returned by `Au.script.run`.

##### Returns

`bool?`

`true` if ended, `false` if failed, `null` if wasn't running.

##### Exceptions

- `ArgumentException`:
    *processId* is 0 or id of this process.

#### Remarks

The script process can be started from editor or not.

The process executes process exit event handlers. Does not execute `finally` code blocks and GC.

Returns `null` if *processId* is invalid (probably because the script is already ended). Returns `false` if *processId* is valid but not of a script process (probably the script ended long time ago and the id is reused for another process).

* * *

## Overload 3

Ends all task processes of a script.

```
public static bool? end(string name)
```

##### Parameters

- *name*  (`string`):
    Script file name (like `"Script43.cs"`) or path in workspace (like `@"\Folder\Script43.cs"`), or full file path.

##### Returns

`bool?`

`true` if ended, `false` if failed (probably file not found), `null` if wasn't running.

##### Exceptions

- `Au.Types.AuException`:
    Editor process not found.

#### Remarks

Can end only script processes started from the editor.

The process executes process exit event handlers. Does not execute `finally` code blocks and GC.