# Method `Au.clipboardData.getImage`

Gets image from the clipboard. Uses clipboard format `Au.Types.ClipFormats.Png` or `Au.Types.ClipFormats.Image` (`CF_BITMAP`).

```
public static Bitmap getImage(bool? png = null)
```

##### Parameters

- *png*  (`bool?`):

    Use PNG format (it supports transparency):

    - `false` - no, only `CF_BITMAP`.
    - `true` - yes, only PNG.
    - `null` (default) - yes, but get `CF_BITMAP` if there is no PNG.

##### Returns

`Bitmap`

`null` if there is no data of this format.

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).
- `Exception`:
    Exceptions of `System.Drawing.Image.FromHbitmap` or `System.Drawing.Image.FromStream`.