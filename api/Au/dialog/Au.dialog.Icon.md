# Method `Au.dialog.Icon`

## Overload 1

Sets common icon.

```
public dialog Icon(DIcon icon)
```

##### Parameters

- *icon*  (`Au.Types.DIcon`)

##### Returns

`Au.dialog`

#### Remarks

The value also can be a native icon group resource id (cast to `Au.Types.DIcon`), in range 1 to 0xf000.

* * *

## Overload 2

Sets custom icon.

```
public dialog Icon(object icon)
```

##### Parameters

- *icon*  (`object`):

    Can be:

    - `Au.icon`.
    - `System.Drawing.Icon`.
    - `IntPtr` - native icon handle.
    - `System.Drawing.Bitmap`.
    - string - XAML image, eg copied from the **Icons** tool. See `Au.More.ImageUtil.LoadGdipBitmapFromXaml`.

##### Returns

`Au.dialog`

#### Remarks

The icon should be of logical size 32 or 16.