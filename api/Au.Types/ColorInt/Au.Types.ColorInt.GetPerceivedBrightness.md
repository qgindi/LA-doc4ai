# Method `Au.Types.ColorInt.GetPerceivedBrightness`

Calculates color's perceived brightness.

```
public static float GetPerceivedBrightness(int color, bool bgr)
```

##### Parameters

- *color*  (`int`):
    Color in `0xRRGGBB` or `0xBBGGRR` format, depending on *bgr*. Ignores alpha.
- *bgr*  (`bool`):
    *color* is in `0xBBGGRR` format. If `false`, `0xRRGGBB`.

##### Returns

`float`

0 to 1.

#### Remarks

Unlike `Au.Types.ColorInt.ToHLS` and `System.Drawing.Color.GetBrightness`, this function uses different weights for red, green and blue components. Ignores alpha.