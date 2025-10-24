# Property `Au.Types.OKey.TextSpeed`

How long to wait (milliseconds) between pressing and releasing each character key. Used by `Au.keys.sendt`. Also by `Au.keys.send` and similar functions for `"!text"` arguments. Default: 0.

```
public int TextSpeed { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 1000 (1 second).

#### Remarks

Used only for "text" arguments, not for "keys" arguments. See `Au.Types.OKey.KeySpeed`.

#### Examples

```
opt.key.TextSpeed = 50;
```