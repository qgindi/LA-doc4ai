# Method `Au.icon.ToGdipBitmap`

Converts native icon to GDI+ bitmap object.

```
public Bitmap ToGdipBitmap(bool destroyIcon = true)
```

##### Parameters

- *destroyIcon*  (`bool`):
    If `true` (default), destroys the native icon object; also clears this variable and don't need to dispose it. If `false`, later will need to dispose this variable.

##### Returns

`Bitmap`

`null` if `Au.icon.Handle` is `default(IntPtr)` or if fails to convert.