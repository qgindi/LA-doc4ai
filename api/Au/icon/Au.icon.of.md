# Method `Au.icon.of`

Gets icon that can be displayed for a file, folder, shell object, URL or file type.

```
public static icon of(string file, int size = 16, IconGetFlags flags = 0)
```

##### Parameters

- *file*  (`string`):

    Can be:

    - Path of any file or folder. Supports environment variables. If not full path, uses `Au.folders.ThisAppImages` and `Au.filesystem.searchPath`.
    - Any shell object, like `":: ITEMIDLIST"`, `@"::{CLSID-1}\::{CLSID-2}"`, `@"shell:AppsFolder\WinStoreAppId"`.
    - File type like `".txt"`, or protocol like `"http:"`. Use `"."` to get folder icon.
    - Path with icon resource index or negative id, like `"c:\file.dll,4"`, `"c:\file.exe,-4"`.
    - URL.
- *size*  (`int`):
    Icon width and height. Default 16.
- *flags*  (`Au.Types.IconGetFlags`)

##### Returns

`Au.icon`

`null` if failed.

#### Remarks

`ITEMIDLIST` can be of any file, folder, URL or a non-filesystem shell object. See `Au.Types.Pidl.ToHexString`.