# Method `Au.folders.sourceCodeMain`

Gets folder path of the main source code file of this program or of a library.

```
public static FolderPath sourceCodeMain(Assembly asm = null)
```

##### Parameters

- *asm*  (`Assembly`):
    An assembly compiled by LibreAutomate. If `null`, uses `System.Reflection.Assembly.GetEntryAssembly`.

##### Returns

`Au.Types.FolderPath`

### See Also

`Au.script.sourcePath`