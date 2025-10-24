# Method `Au.script.sourcePath`

## Overload 1

Gets path of the caller source code file.

```
public static string sourcePath(string f_ = null)
```

##### Parameters

- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`string`

### See Also

`System.Runtime.CompilerServices.CallerFilePathAttribute`

`Au.folders.sourceCode`

* * *

## Overload 2

Gets path of the main source code file of this program or of a library.

```
public static string sourcePath(bool inWorkspace, Assembly asm = null)
```

##### Parameters

- *inWorkspace*  (`bool`):
    Get path in the workspace, like `@"\Script1.cs"` or `@"\Folder1\Script1.cs"`.
- *asm*  (`Assembly`):
    An assembly compiled by LibreAutomate. If `null`, uses `System.Reflection.Assembly.GetEntryAssembly`.

##### Returns

`string`

`null` if failed.

#### Remarks

When compiling, LibreAutomate adds `Au.Types.PathInWorkspaceAttribute` to the assembly. Then at run time this function gets its value. Returns `null` if compiled by some other compiler.

### See Also

`Au.folders.sourceCodeMain`