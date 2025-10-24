# Constructor of `Au.wpfBuilder`

## Overload 1

This constructor creates `System.Windows.Window` object with panel of specified type (default is `System.Windows.Controls.Grid`).

```
public wpfBuilder(string windowTitle, WBPanelType panelType = WBPanelType.Grid)
```

##### Parameters

- *windowTitle*  (`string`):
    Window title bar text.
- *panelType*  (`Au.Types.WBPanelType`):
    Panel type. Default is `System.Windows.Controls.Grid`. Later you also can add nested panels of various types with `StartX` functions.

* * *

## Overload 2

This constructor creates panel of specified type (default is `System.Windows.Controls.Grid`) and optionally adds to a container.

```
public wpfBuilder(FrameworkElement container = null, WBPanelType panelType = WBPanelType.Grid, bool setProperties = true)
```

##### Parameters

- *container*  (`FrameworkElement`):
    Window or some other element that will contain the panel. Should be empty, unless the type supports multiple direct child elements. Can be `null`. If the type (or base type) is `System.Windows.Controls.ContentControl` (`System.Windows.Window`, `System.Windows.Controls.TabItem`, `System.Windows.Controls.ToolTip`, etc), `System.Windows.Controls.Primitives.Popup` or `System.Windows.Controls.Decorator` (eg `Border`), this function adds the panel to it. If *container* is `null` or an element of some other type, need to explicitly add the panel to it, like `container.Child = b.Panel;` or `container.Children.Add(b.Panel);` or `b.Tooltip(btt.Panel);` or `hwndSource.RootVisual = btt.Panel;` (the code depends on *container* type).
- *panelType*  (`Au.Types.WBPanelType`):
    Panel type. Default is `System.Windows.Controls.Grid`. Later you also can add nested panels of various types with `StartX` functions.
- *setProperties*  (`bool`):

    Set some container's properties like other overload does. Default `true`. Currently sets these properties, and only if *container* is of type `Window`:

    - `System.Windows.Window.SizeToContent`, except when *container* is `Canvas` or has properties `Width` and/or `Height` set.
    - `SnapsToDevicePixels` = `true`.
    - `WindowStartupLocation` = `Center`.
    - `Topmost` and `Background` depending on static properties `Au.wpfBuilder.winTopmost` and `Au.wpfBuilder.winWhite`.