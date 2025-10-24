# Property `Au.toolbar.Offsets`

Specifies distances between edges of the toolbar and edges of its owner, depending on `Au.toolbar.Anchor`.

```
public TBOffsets Offsets { get; set; }
```

##### Property Value

`Au.Types.TBOffsets`

#### Remarks

Owner is specified when calling `Au.toolbar.Show`. It can be a window, screen, control or other object.

The `Au.Types.TBOffsets` type has 4 properties - `Top`, `Bottom`, `Left` and `Right`, but used are only those included in `Au.toolbar.Anchor`. For example, if `Anchor` is `TopLeft`, used are only `Top` and `Left`.

The unit of measurement depends on `Au.toolbar.DpiScaling` and whether anchor is screen.

This property is updated when moving or resizing the toolbar. It is saved.

#### Examples

```
t.Offsets = new(150, 5, 0, 0);
```