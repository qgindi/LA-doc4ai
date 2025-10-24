# Class `Au.More.MouseCursor`

Helps to load cursors, etc. Contains native cursor handle.

```
public class MouseCursor
```

##### Remarks

To load cursors for winforms can be used `System.Windows.Forms.Cursor` constructors, but they don't support colors, ani cursors and custom size. Don't use this class to load cursors for WPF. Its `Cursor` class loads cursors correctly.

##### Inheritance

`object` → `MouseCursor`

### Constructors

`MouseCursor(nint)`

### Properties

`Handle`

### Methods

`Dispose`, `GetCurrentVisibleCursor`, `Hash`, `Load`, `Load`, `ToGdipCursor`