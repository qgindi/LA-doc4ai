# Method `Au.Types.ColorInt.FromBGR`

Converts from Windows native `COLORREF` (`0xBBGGRR` to `0xAARRGGBB`).

```
public static ColorInt FromBGR(int colorBGR, bool? makeOpaque = null)
```

##### Parameters

- *colorBGR*  (`int`):
    Color in `0xBBGGRR` format.
- *makeOpaque*  (`bool?`):
    Set alpha = 0xFF. If `null` (default), sets alpha = 0xFF if it is 0 in *colorBGR*.

##### Returns

`Au.Types.ColorInt`