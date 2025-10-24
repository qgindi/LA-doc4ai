# Class `Au.More.GridSplitter2`

Grid splitter control. Based on `System.Windows.Controls.GridSplitter`, changes its behavior.

```
public class GridSplitter2 : GridSplitter, IAnimatable, ISupportInitialize, IFrameworkInputElement, IInputElement, IQueryAmbient
```

##### Remarks

Try this class when `System.Windows.Controls.GridSplitter` does not work as you want.

Limitations (bad or good):

- Splitters must be on own rows/columns. Throws exception if `ResizeBehavior` is not `PreviousAndNext` (which is default).
- Throws exception is there are star-sized splitter rows.
- Does not resize auto-sized rows/columns. Only pixel-sized and star-sized.
- With `UseLayoutRounding` may flicker when resizing, especially when high DPI.

##### Inheritance

`object` → `DispatcherObject` → `DependencyObject` → `Visual` → `UIElement` → `FrameworkElement` → `Control` → `Thumb` → `GridSplitter` → `GridSplitter2`

### Constructors

`GridSplitter2()`

### Properties

`ResizeNearest`

### Methods

`OnKeyDown`