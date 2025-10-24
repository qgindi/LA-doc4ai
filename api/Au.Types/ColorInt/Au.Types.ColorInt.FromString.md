# Method `Au.Types.ColorInt.FromString`

Converts from a color name (`System.Drawing.Color.FromName`) or string `"0xRRGGBB"` or `"#RRGGBB"`.

```
public static bool FromString(string s, out ColorInt c)
```

##### Parameters

- *s*  (`string`)
- *c*  (`Au.Types.ColorInt`)

##### Returns

`bool`

#### Remarks

If *s* is a hex number that contains 6 or less hex digits, makes opaque (alpha 0xFF). If *s* is `null` or invalid, sets `c.argb = 0` and returns `false`.