# Method `Au.folders.unexpandPath`

## Overload 1

If string starts with a known/special folder path, gets folder name + relative path and returns `true`. For example if string is `"C:\Windows\System32\notepad.exe"`, gets `"folders.System"` and `"notepad.exe"`.

```
public static bool unexpandPath(string path, out string folder, out string name)
```

##### Parameters

- *path*  (`string`):
    Any string. Can be `null`. Case-insensitive. Supports `":: ITEMIDLIST"` (see `Au.Types.Pidl.ToHexString`).
- *folder*  (`string`):
    Receives special folder string like `"folders.System"`.
- *name*  (`string`):
    Receives filename or relative path in the folder.

##### Returns

`bool`

#### Remarks

Quite slow first time in process, eg 50 ms, because gets all folder paths. Later uses cached paths.

### See Also

`Au.pathname.expand`

* * *

## Overload 2

If string starts with a known/special folder path, replaces that part with `%folders.FolderName%`. Else returns unchanged string. For example if string is `"C:\Windows\System32\notepad.exe"`, returns `"%folders.System%\notepad.exe"`.

```
public static string unexpandPath(string path)
```

##### Parameters

- *path*  (`string`):
    Any string. Can be `null`. Case-insensitive. Supports `":: ITEMIDLIST"` (see `Au.Types.Pidl.ToHexString`).

##### Returns

`string`

* * *

## Overload 3

If *path* starts with one of specified folder paths, replaces that part with the replacements string. Else returns unchanged string.

```
public static string unexpandPath(string path, params (string folder, string replacement)[] list)
```

##### Parameters

- *path*  (`string`):
    Any string. Can be `null`. Case-insensitive.
- *list*  (`(string folder, string replacement)[]`):
    Folder paths and replacement strings.

##### Returns

`string`

#### Examples

```
var s = folders.Documents + "file.txt";
//var s = folders.Temp + "file.txt";
print.it(s);
print.it(folders.unexpandPath(s, (folders.Temp, "%temp%"), (folders.Documents, "%folders.Documents%")));
```