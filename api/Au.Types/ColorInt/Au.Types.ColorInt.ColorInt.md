# Constructor of `Au.Types.ColorInt`

## Overload 1

```
public ColorInt(int colorARGB, bool? makeOpaque = null)
```

##### Parameters

- *colorARGB*  (`int`):
    Color value in `0xAARRGGBB` or `0xRRGGBB` format.
- *makeOpaque*  (`bool?`):
    Set alpha = 0xFF. If `null` (default), sets alpha = 0xFF if it is 0 in *colorBGR*.

* * *

## Overload 2

```
public ColorInt(uint colorARGB, bool? makeOpaque)
```

##### Parameters

- *colorARGB*  (`uint`):
    Color value in `0xAARRGGBB` or `0xRRGGBB` format.
- *makeOpaque*  (`bool?`):
    Set alpha = 0xFF. If `null` (default), sets alpha = 0xFF if it is 0 in *colorBGR*.