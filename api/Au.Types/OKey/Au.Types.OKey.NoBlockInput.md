# Property `Au.Types.OKey.NoBlockInput`

While sending or pasting keys or text, don't block user-pressed keys. Default: `false`.

```
public bool NoBlockInput { get; set; }
```

##### Property Value

`bool`

#### Remarks

If `false` (default), user-pressed keys are sent afterwards. If `true`, user-pressed keys can be mixed with script-pressed keys, which is particularly dangerous when modifier keys are mixed (and combined) with non-modifier keys.

#### Examples

```
opt.key.NoBlockInput = true;
```