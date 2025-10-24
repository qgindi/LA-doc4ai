# Property `Au.toolbar.Anchor`

Specifies to which owner's edges the toolbar keeps constant distance when moving or resizing the owner.

```
public TBAnchor Anchor { get; set; }
```

##### Property Value

`Au.Types.TBAnchor`

#### Remarks

The owner can be a window, screen, control or other object. It is specified when calling `Au.toolbar.Show`. This property is in the context menu and is saved.

### See Also

`Au.toolbar.Offsets`