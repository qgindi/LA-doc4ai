# Method `Au.script.restart`

Starts this script or program again.

```
public static int restart(params string[] args)
```

##### Parameters

- *args*  (`string[]`):
    Command line arguments. Should not contain `'\0'` characters.

##### Returns

`int`

Native process id of the new process. Returns -1 if failed.

##### Exceptions

- `FileNotFoundException`:
    Script file not found.
- `InvalidOperationException`:
    This script has role `editorExtension`.

#### Remarks

Does not end this process. The new process runs simultaneously, like with `/*/ ifRunning run; /*/`. Let this process exit as it wants, for example return from the main script code.

If this process was started by LibreAutomate, the new process will be started by LibreAutomate too. Else this function simply starts a new instance of this program.