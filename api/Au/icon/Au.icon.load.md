# Method `Au.icon.load`

Extracts icon directly from file.

```
public static icon load(string file, int size = 16, int index = 0)
```

##### Parameters

- *file*  (`string`):
    `.ico`, `.exe`, `.dll` or other file that contains one or more icons. Also supports cursor files - `.cur`, `.ani`. Must be full path, without icon index. Supports environment variables (see `Au.pathname.expand`).
- *size*  (`int`):
    Icon width and height. Default 16.
- *index*  (`int`):
    Icon index or negative icon resource id in the `.exe`/`.dll` file.

##### Returns

`Au.icon`

`null` if failed.