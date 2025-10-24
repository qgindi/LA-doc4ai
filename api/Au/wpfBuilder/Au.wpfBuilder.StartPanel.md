# Method `Au.wpfBuilder.StartPanel`

## Overload 1

Adds panel of any type. It will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartPanel(Panel panel, bool childOfLast = false)
```

##### Parameters

- *panel*  (`Panel`):
    New panel of any type (`System.Windows.Controls.Grid`, `System.Windows.Controls.WrapPanel`, etc). For `System.Windows.Controls.Grid` and `System.Windows.Controls.Canvas` this function sets some panel properties to make everything work like with other `StartX` functions.
- *childOfLast*  (`bool`):
    Add as a child or content of the last added element (`Au.wpfBuilder.Last`), which must be a `System.Windows.Controls.Decorator` (for example `System.Windows.Controls.Border` or `System.Windows.Documents.AdornerDecorator`) or `System.Windows.Controls.ContentControl` (for example `System.Windows.Controls.Button`).

##### Returns

`Au.wpfBuilder`

* * *

## Overload 2

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child panel of any type. The panel will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartPanel<TContainer>(Panel panel, object header) where TContainer : HeaderedContentControl, new()
```

##### Parameters

- *panel*  (`Panel`):
    New panel of any type (`System.Windows.Controls.Grid`, `System.Windows.Controls.WrapPanel`, etc). For `System.Windows.Controls.Grid` and `System.Windows.Controls.Canvas` this function sets some panel properties to make everything work like with other `StartX` functions.
- *header*  (`object`):
    Header text/content.

##### Returns

`Au.wpfBuilder`

##### Type Parameters

- `TContainer`:
    Any `System.Windows.Controls.HeaderedContentControl`-based type.