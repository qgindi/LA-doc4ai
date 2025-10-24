# Property `Au.Types.OKey.PasteWorkaround`

When pasting text that ends with space, tab or/and newline characters, remove them and after pasting send them as keys. Default: `false`.

```
public bool PasteWorkaround { get; set; }
```

##### Property Value

`bool`

#### Remarks

Some apps trim these characters when pasting.

#### Examples

```
opt.key.PasteWorkaround = true;
```