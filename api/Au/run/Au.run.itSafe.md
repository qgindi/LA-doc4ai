# Method `Au.run.itSafe`

Calls `Au.run.it` and handles exceptions. If `Au.run.it` throws exception, writes it to the output as warning and returns `null`.

```
public static RResult itSafe(string file, string args = null, RFlags flags = 0, ROptions dirEtc = null)
```

##### Parameters

- *file*  (`string`):

    Examples:

    - `@"C:\file.txt"`
    - `folders.Documents`
    - `folders.System + "notepad.exe"`
    - `@"%folders.System%\notepad.exe"`
    - `@"%TMP%\file.txt"`
    - `"notepad.exe"`
    - `@"..\folder\x.exe"`
    - `"http://a.b.c/d"`
    - `"file:///path"`
    - `"mailto:a@b.c"`
    - `":: ITEMIDLIST"`
    - `@"shell:::{CLSID}"`
    - `@"shell:AppsFolder\Microsoft.WindowsCalculator_8wekyb3d8bbwe!App"`.
- *args*  (`string`):
    Command line arguments. This function expands environment variables if starts with `"%"` or `"\"%"`.
- *flags*  (`Au.Types.RFlags`)
- *dirEtc*  (`Au.Types.ROptions`):
    Allows to specify more parameters: current directory, verb, etc. If string, it sets initial current directory for the new process. If `""`, gets it from *file*. More info: `Au.Types.ROptions.CurrentDirectory`.

##### Returns

`Au.Types.RResult`

#### Remarks

This function is useful when you don't care whether `Au.run.it` succeeded and don't want to use try/catch. Handles only exception of type `Au.Types.AuException`. It is thrown when fails, usually when the file does not exist.

### See Also

`Au.print.warning`

`Au.Types.OWarnings.Disable`

`Au.wnd.findOrRun`