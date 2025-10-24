# Method `Au.icon.parsePathIndex`

Parses icon location string.

```
public static bool parsePathIndex(string s, out string path, out int index)
```

##### Parameters

- *s*  (`string`):
    Icon location. Can be `"path,index"` or `"path,-id"` or just path. Supports path enclosed in `""` like `"\"path\",index"`, and spaces between comma and index like `"path, index"`.
- *path*  (`string`):
    Receives path without index and without `""`. Can be the same variable as *s*.
- *index*  (`int`):
    Receives index/id or 0.

##### Returns

`bool`

`true` if it includes icon index or resource id.