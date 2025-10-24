# Property `Au.osdText.XY`

Coordinates. Default: `null` (screen center).

```
public PopupXY XY { get; set; }
```

##### Property Value

`Au.Types.PopupXY`

#### Remarks

Not used if `Au.osdText.Rect` is set. This property can be changed after creating OSD window.

#### Examples

```
var m = new osdText { Text = "Text" };
m.XY = new(Coord.Center, Coord.Max); //bottom-center of the work area of the primary screen
m.Show();
```