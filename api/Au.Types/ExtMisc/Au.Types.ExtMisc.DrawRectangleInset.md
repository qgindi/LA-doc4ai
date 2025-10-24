# Method `Au.Types.ExtMisc.DrawRectangleInset`

## Overload 1

Draws inset or outset rectangle.

```
public static void DrawRectangleInset(this Graphics t, Pen pen, RECT r, bool outset = false)
```

##### Parameters

- *t*  (`Graphics`)
- *pen*  (`Pen`):
    Pen with integer width and default alignment.
- *r*  (`Au.Types.RECT`)
- *outset*  (`bool`):
    Draw outset.

#### Remarks

Calls `System.Drawing.Graphics.DrawRectangle` with arguments corrected so that it draws inside or outside *r*. Does not use `System.Drawing.Drawing2D.PenAlignment`, it is unreliable.

* * *

## Overload 2

Draws inset rectangle of specified pen color and width.

```
public static void DrawRectangleInset(this Graphics t, Color penColor, int penWidth, RECT r, bool outset = false)
```

##### Parameters

- *t*  (`Graphics`)
- *penColor*  (`Color`)
- *penWidth*  (`int`)
- *r*  (`Au.Types.RECT`)
- *outset*  (`bool`)

#### Remarks

Creates pen and calls other overload.