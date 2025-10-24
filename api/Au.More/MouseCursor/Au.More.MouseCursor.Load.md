# Method `Au.More.MouseCursor.Load`

## Overload 1

Loads cursor from file.

```
public static MouseCursor Load(string file, int size = 0)
```

##### Parameters

- *file*  (`string`):
    `.cur` or `.ani` file. If not full path, uses `Au.folders.ThisAppImages`.
- *size*  (`int`):
    Width and height. If 0, uses system default size, which depends on DPI.

##### Returns

`Au.More.MouseCursor`

`default(MouseCursor)` if failed.

* * *

## Overload 2

Creates cursor from cursor file data in memory, for example from a managed resource.

```
public static MouseCursor Load(byte[] cursorData, int size = 0)
```

##### Parameters

- *cursorData*  (`byte[]`):
    Data of `.cur` or `.ani` file.
- *size*  (`int`):
    Width and height. If 0, uses system default size, which depends on DPI.

##### Returns

`Au.More.MouseCursor`

`default(MouseCursor)` if failed.

#### Remarks

This function creates/deletes a temporary file, because there is no good API to load cursor from memory.