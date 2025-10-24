# Property `Au.Types.OKey.KeySpeed`

How long to wait (milliseconds) between pressing and releasing each key. Used by `Au.keys.send` and similar functions, except for `"!text"` arguments. Default: 2.

```
public int KeySpeed { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 1000 (1 second).

#### Remarks

Used only for "keys" arguments, not for "text" arguments. See `Au.Types.OKey.TextSpeed`.

#### Examples

```
opt.key.KeySpeed = 50;
```