# Method `Au.clipboardData.AddImage`

Adds image. Uses clipboard format `Au.Types.ClipFormats.Png` and/or `Au.Types.ClipFormats.Image` (`CF_BITMAP`).

```
public clipboardData AddImage(Image image, bool? png = null)
```

##### Parameters

- *image*  (`Image`):
    Image. Must be `System.Drawing.Bitmap`, else exception.
- *png*  (`bool?`):

    Use PNG format (it supports transparency):

    - `false` - no, only `CF_BITMAP`.
    - `true` - yes, only PNG.
    - `null` (default) - add PNG and `CF_BITMAP`.

##### Returns

`Au.clipboardData`

this.

##### Exceptions

- `ArgumentNullException`