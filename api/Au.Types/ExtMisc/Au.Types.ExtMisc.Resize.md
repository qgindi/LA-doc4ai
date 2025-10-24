# Method `Au.Types.ExtMisc.Resize`

## Overload 1

Resizes this image.

```
public static Bitmap Resize(this Bitmap b, int width, int height, BRFilter filter, bool dispose, bool premultiplied = false)
```

##### Parameters

- *b*  (`Bitmap`)
- *width*  (`int`):
    New width.
- *height*  (`int`):
    New height. If *width* or *height* is 0, calculates it (preserves aspect ratio).
- *filter*  (`Au.Types.BRFilter`)
- *dispose*  (`bool`):
    When resized, call `Dispose` for this object.
- *premultiplied*  (`bool`):
    Let the resized bitmap have `PixelFormat` = `Format32bppPArgb`. It prevents distortions at transparent-opaque boundaries. If `false`: if this bitmap has `Format32bppArgb` or `Format32bppPArgb`, does not change, else `PixelFormat.Format32bppArgb`.

##### Returns

`Bitmap`

Resized image (new object). Returns this image if new width and height would be the same as of this image.

##### Exceptions

- `ArgumentException`:
    Unsupported `PixelFormat`.

* * *

## Overload 2

Resizes this image.

```
public static Bitmap Resize(this Bitmap b, double factor, BRFilter filter, bool dispose, bool premultiplied = false)
```

##### Parameters

- *b*  (`Bitmap`)
- *factor*  (`double`):
    Scaling factor. For example 2 to make 2 times bigger, or 0.5 to make 2 times smaller.
- *filter*  (`Au.Types.BRFilter`)
- *dispose*  (`bool`):
    When resized, call `Dispose` for this object.
- *premultiplied*  (`bool`):
    Let the resized bitmap have `PixelFormat` = `Format32bppPArgb`. It prevents distortions at transparent-opaque boundaries. If `false`: if this bitmap has `Format32bppArgb` or `Format32bppPArgb`, does not change, else `PixelFormat.Format32bppArgb`.

##### Returns

`Bitmap`

Resized image (new object). Returns this image if new width and height would be the same as of this image.

##### Exceptions

- `ArgumentException`:
    Unsupported `PixelFormat`.