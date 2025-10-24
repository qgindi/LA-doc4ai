# Method `Au.script.writeResult`

Writes a string result for the task that called `Au.script.runWait` or `Au.script.runWait` to run this task, or for the program that started this task using command line like `"Au.Editor.exe *Script5.cs"`.

```
public static bool writeResult(string s)
```

##### Parameters

- *s*  (`string`):
    A string. This function does not append newline characters.

##### Returns

`bool`

`false` if this task was not started in such a way. Or if failed to write, except when *s* is `null`/`""`.

#### Remarks

`Au.script.runWait` can read the string in real time. `Au.script.runWait` gets all strings joined when the task ends. The program that started this task using command line like `"Au.Editor.exe *Script5.cs"` can read the string from the redirected standard output in real time, or the string is displayed to its console in real time. The string encoding is UTF-8; if you use a `.bat` file or `cmd.exe` and want to get correct Unicode text, execute this before, to change console code page to UTF-8: `chcp 65001`.

Does not work if script role is `editorExtension`.