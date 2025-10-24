# Method `Au.script.single`

Ensures that multiple processes that call this function don't run simultaneously. Like C# `lock` keyword for threads.

```
public static void single(string mutex = "Au-mutex-script.single", int wait = 0, bool silent = false, Action ifCantRun = null)
```

##### Parameters

- *mutex*  (`string`):
    Mutex name. If another process called this function with this mutex name, this process cannot run, and this function calls `Environment.Exit(3);`.
- *wait*  (`int`):
    Milliseconds to wait until this process can run. No timeout if -1.
- *silent*  (`bool`):
    Don't print `"cannot run"`.
- *ifCantRun*  (`Action`):
    Called if this process cannot run.

##### Exceptions

- `InvalidOperationException`:
    This function already called.

#### Remarks

This function is useful when this script has role `exeProgram` and the compiled program is launched not from the script editor, because then the `/*/ ifRunning /*/` property is ignored.

### See Also

`Au.More.AppSingleInstance`