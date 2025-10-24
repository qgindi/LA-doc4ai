# Operator `Au.Types.FolderPath.operator +`

Calls `Au.pathname.combine`. Example: `string s = folders.Desktop + "file.txt";`

```
public static string operator +(FolderPath fp, string append)
```

##### Parameters

- *fp*  (`Au.Types.FolderPath`)
- *append*  (`string`)

##### Returns

`string`

##### Exceptions

- `ArgumentException`:
    *fp* is empty.