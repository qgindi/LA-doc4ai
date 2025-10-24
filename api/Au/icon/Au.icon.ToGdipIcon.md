# Method `Au.icon.ToGdipIcon`

Creates `System.Drawing.Icon` object that shares native icon handle with this object.

```
public Icon ToGdipIcon()
```

##### Returns

`Icon`

`null` if `Au.icon.Handle` is `default(IntPtr)`.