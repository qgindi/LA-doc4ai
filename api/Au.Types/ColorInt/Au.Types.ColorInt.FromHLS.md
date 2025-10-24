# Method `Au.Types.ColorInt.FromHLS`

Converts from hue-luminance-saturation (HLS).

```
public static int FromHLS(int H, int L, int S, bool bgr)
```

##### Parameters

- *H*  (`int`):
    Hue, 0 to 240.
- *L*  (`int`):
    Luminance, 0 to 240.
- *S*  (`int`):
    Saturation, 0 to 240.
- *bgr*  (`bool`):
    Return color in `0xBBGGRR` format. If `false`, `0xRRGGBB`.

##### Returns

`int`

Color in `0xRRGGBB` or `0xBBGGRR` format, depending on *bgr*. Alpha 0.