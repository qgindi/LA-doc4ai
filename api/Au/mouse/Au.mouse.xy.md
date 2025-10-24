# Property `Au.mouse.xy`

Gets cursor (mouse pointer) position.

```
public static POINT xy { get; }
```

##### Property Value

`Au.Types.POINT`

#### Examples

```
var p = mouse.xy;
print.it(p.x, p.y);

var (x, y) = mouse.xy;
print.it(x, y);
```

```
POINT mousePos = mouse.xy;
mouse.moveBy(20, 50);
POINT mousePos2 = mouse.xy;

double dist = Math2.Distance(mousePos2, mousePos);
print.it(dist, (int)dist, dist.ToInt(), mousePos2.x - mousePos.x, mousePos2.y - mousePos.y);
```