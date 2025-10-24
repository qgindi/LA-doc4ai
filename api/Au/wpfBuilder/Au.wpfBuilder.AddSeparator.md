# Method `Au.wpfBuilder.AddSeparator`

Adds `System.Windows.Controls.Separator` control.

```
public wpfBuilder AddSeparator(bool? vertical = null)
```

##### Parameters

- *vertical*  (`bool?`):
    If `true`, adds vertical separator. If `false`, horizontal. If `null` (default), adds vertical if in horizontal stack panel, else adds horizontal.

##### Returns

`Au.wpfBuilder`

#### Remarks

In `System.Windows.Controls.Canvas` panel separator's default size is 1x1. Need to set size, like `.AddSeparator().XY(0, 50, 100, 1)`.