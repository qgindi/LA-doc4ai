# Method `Au.Types.ColorInt.ToBGR`

Converts to Windows native `COLORREF` (`0xBBGGRR` from `0xAARRGGBB`).

```
public int ToBGR(bool zeroAlpha = true)
```

##### Parameters

- *zeroAlpha*  (`bool`):
    Set the alpha byte = 0.

##### Returns

`int`

color in `COLORREF` format. Does not modify this variable.