# Property `Au.osdText.defaultScreen`

Default screen when `Au.osdText.XY` is not set. The `Au.screen` must be lazy or empty.

```
public static screen defaultScreen { get; set; }
```

##### Exceptions

- `ArgumentException`:
    `Au.screen` with `Handle`. Must be lazy (with `Au.screen.LazyFunc`) or empty.

##### Property Value

`Au.screen`

#### Examples

```
osdText.defaultScreen = screen.index(1, lazy: true);
```