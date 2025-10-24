# Method `Au.Types.ColorInt.ToHLS`

Converts to hue-luminance-saturation (HLS).

```
public static (int H, int L, int S) ToHLS(int color, bool bgr)
```

##### Parameters

- *color*  (`int`):
    Color in `0xRRGGBB` or `0xBBGGRR` format, depending on *bgr*. Ignores alpha.
- *bgr*  (`bool`):
    *color* is in `0xBBGGRR` format. If `false`, `0xRRGGBB`.

##### Returns

`(int H, int L, int S)`

Hue, luminance and saturation. All 0 to 240.