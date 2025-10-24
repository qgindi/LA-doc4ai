# Constructor of `Au.More.MemoryBitmap`

## Overload 1

Does nothing. Later you can call `Au.More.MemoryBitmap.Create` or `Au.More.MemoryBitmap.Attach`.

```
public MemoryBitmap()
```

* * *

## Overload 2

Calls `Au.More.MemoryBitmap.Create`.

```
public MemoryBitmap(int width, int height)
```

##### Parameters

- *width*  (`int`)
- *height*  (`int`)

##### Exceptions

- `ArgumentException`:
    *width* or *height* is less than 1.
- `Au.Types.AuException`:
    Failed. Probably there is not enough memory for bitmap of specified size (need `with*height*4` bytes).