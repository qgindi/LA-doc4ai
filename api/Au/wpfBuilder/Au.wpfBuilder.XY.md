# Method `Au.wpfBuilder.XY`

Sets position of the last added element in `System.Windows.Controls.Canvas` panel. Optionally sets size.

```
public wpfBuilder XY(double x, double y, WBLength? width = null, WBLength? height = null)
```

##### Parameters

- *x*  (`double`)
- *y*  (`double`)
- *width*  (`Au.Types.WBLength?`):
    Width or/and min/max width.
- *height*  (`Au.Types.WBLength?`):
    Height or/and min/max height.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    Current panel is not `System.Windows.Controls.Canvas`.

#### Remarks

Only in `System.Windows.Controls.Canvas` panel you can set position explicitly. In other panel types it is set automatically and can be adjusted with `Au.wpfBuilder.Margin`, `Au.wpfBuilder.Align`, container's `Au.wpfBuilder.AlignContent`, etc.