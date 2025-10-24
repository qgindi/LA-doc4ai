# Method `Au.More.MemoryBitmap.Create`

Creates new memory DC and bitmap of specified size and selects it into the DC.

```
public bool Create(int width, int height)
```

##### Parameters

- *width*  (`int`):
    Width, pixels. Must be > 0.
- *height*  (`int`):
    Height, pixels. Must be > 0.

##### Returns

`bool`

`false` if failed. In any case deletes previous bitmap and DC.