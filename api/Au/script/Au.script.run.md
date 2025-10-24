# Method `Au.script.run`

Starts executing a script. Does not wait.

```
public static int run(string script, params string[] args)
```

##### Parameters

- *script*  (`string`):
    Script name like `"Script5.cs"`, or path like `@"\Folder\Script5.cs"`.
- *args*  (`string[]`):
    Command line arguments. In the script it will be variable *args*. Should not contain `'\0'` characters.

##### Returns

`int`

Native process id of the task process. Returns -1 if failed, for example if the script contains errors or cannot run second task instance. Returns 0 if task start is deferred because the script is running (`ifRunning` `wait`/`wait_restart`). If role `editorExtension`, waits until the script ends, then returns 0.

##### Exceptions

- `FileNotFoundException`:
    Script file not found.
- `Au.Types.AuException`:
    Script editor not running.