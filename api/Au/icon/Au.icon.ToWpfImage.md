# Method `Au.icon.ToWpfImage`

Converts native icon to WPF image object.

```
public BitmapSource ToWpfImage(bool destroyIcon = true)
```

##### Parameters

- *destroyIcon*  (`bool`):
    If `true` (default), destroys the native icon object; also clears this variable and don't need to dispose it. If `false`, later will need to dispose this variable.

##### Returns

`BitmapSource`

`null` if `Au.icon.Handle` is `default(IntPtr)` or if fails to convert.

#### Remarks

The image is not suitable for WPF window icon. Instead use `Au.icon.SetWindowIcon` or WPF image loading functions.