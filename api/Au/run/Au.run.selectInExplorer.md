# Method `Au.run.selectInExplorer`

Opens parent folder in File Explorer (folder window) and selects the file.

```
public static bool selectInExplorer(string path)
```

##### Parameters

- *path*  (`string`):
    Full path of a file or directory or other shell object. Supports `@"%environmentVariable%\..."` (see `Au.pathname.expand`) and `"::..."` (see `Au.Types.Pidl.ToHexString`).

##### Returns

`bool`

`false` if failed, for example if the file does not exist.