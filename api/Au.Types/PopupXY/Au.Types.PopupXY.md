# Class `Au.Types.PopupXY`

Can be used to specify coordinates for various popup windows, like `new PopupXY(x, y)`, `(x, y)`, `PopupXY.In(rectangle)`, `PopupXY.Mouse`.

```
public class PopupXY
```

##### Inheritance

`object` → `PopupXY`

### Constructors

`PopupXY(Coord, Coord, bool, screen)`

### Fields

`inRect`, `rect`, `screen`, `workArea`, `x`, `y`

### Properties

`Mouse`

### Methods

`GetScreen`, `In`

### Operators

`implicit operator PopupXY(POINT)`, `implicit operator PopupXY((Coord x, Coord y))`