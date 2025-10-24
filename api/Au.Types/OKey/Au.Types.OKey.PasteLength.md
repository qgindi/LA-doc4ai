# Property `Au.Types.OKey.PasteLength`

To send text use clipboard (like with `Au.Types.OKeyText.Paste`) if text length is >= this value. Default: 200.

```
public int PasteLength { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

#### Examples

```
opt.key.PasteLength = 50;
```