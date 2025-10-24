# Method `Au.pathname.expand`

If *path* starts with `"%"` or `"\"%"`, expands environment variables enclosed in `%`, else just returns *path*. Also supports known folder names, like `"%folders.Documents%"`. More info in Remarks.

```
public static string expand(string path, bool? strict = null)
```

##### Parameters

- *path*  (`string`):
    Any string. Can be `null`.
- *strict*  (`bool?`):

    What to do if *path* looks like starts with and environment variable or known folder but the variable/folder does not exist:

    - `true` - throw `System.ArgumentException`;
    - `false` - return unexpanded path;
    - `null` (default) - call `Au.print.warning` and return unexpanded path.

##### Returns

`string`

#### Remarks

Supports known folder names. See `Au.folders`. Example: `@"%folders.Documents%\file.txt"`. Example: `@"%folders.shell.ControlPanel%" //gets ":: ITEMIDLIST"`. Usually known folders are used like `string path = folders.Documents + "file.txt"`. However it cannot be used when you want to store paths in text files, registry, etc. Then this feature is useful. To get known folder path, this function calls `Au.folders.getFolder`.

This function is called by many functions of classes `Au.pathname`, `Au.filesystem`, `Au.icon`, some others, therefore all they support environment variables and known folders in path string.

### See Also

`System.Environment.ExpandEnvironmentVariables`

`System.Environment.GetEnvironmentVariable`

`System.Environment.SetEnvironmentVariable`