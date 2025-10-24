# Method `Au.script.runWait`

## Overload 1

Starts executing a script and waits until the task ends.

```
public static int runWait(string script, params string[] args)
```

##### Parameters

- *script*  (`string`):
    Script name like `"Script5.cs"`, or path like `@"\Folder\Script5.cs"`.
- *args*  (`string[]`):
    Command line arguments. In the script it will be variable *args*. Should not contain `'\0'` characters.

##### Returns

`int`

The exit code of the task process. See `System.Environment.ExitCode`.

##### Exceptions

- `FileNotFoundException`:
    Script file not found.
- `Au.Types.AuException`:
    Failed to start script task. For example: the script contains errors; cannot start second task instance; script editor not running.

* * *

## Overload 2

Starts executing a script, waits until the task ends and then gets `Au.script.writeResult` text.

```
public static int runWait(out string results, string script, params string[] args)
```

##### Parameters

- *results*  (`string`):
    Receives `Au.script.writeResult` text.
- *script*  (`string`):
    Script name like `"Script5.cs"`, or path like `@"\Folder\Script5.cs"`.
- *args*  (`string[]`):
    Command line arguments. In the script it will be variable *args*. Should not contain `'\0'` characters.

##### Returns

`int`

The exit code of the task process. See `System.Environment.ExitCode`.

##### Exceptions

- `FileNotFoundException`:
    Script file not found.
- `Au.Types.AuException`:
    Failed to start script task. For example: the script contains errors; cannot start second task instance; script editor not running.

* * *

## Overload 3

Starts executing a script, waits until the task ends and gets `Au.script.writeResult` text in real time.

```
public static int runWait(Action<string> results, string script, params string[] args)
```

##### Parameters

- *results*  (`Action<string>`):
    Receives `Au.script.writeResult` output whenever the task calls it.
- *script*  (`string`):
    Script name like `"Script5.cs"`, or path like `@"\Folder\Script5.cs"`.
- *args*  (`string[]`):
    Command line arguments. In the script it will be variable *args*. Should not contain `'\0'` characters.

##### Returns

`int`

The exit code of the task process. See `System.Environment.ExitCode`.

##### Exceptions

- `FileNotFoundException`:
    Script file not found.
- `Au.Types.AuException`:
    Failed to start script task. For example: the script contains errors; cannot start second task instance; script editor not running.