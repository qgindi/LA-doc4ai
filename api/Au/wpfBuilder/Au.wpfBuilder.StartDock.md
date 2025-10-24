# Method `Au.wpfBuilder.StartDock`

## Overload 1

Adds `System.Windows.Controls.DockPanel` panel that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartDock(bool childOfLast = false)
```

##### Parameters

- *childOfLast*  (`bool`):
    Add as a child or content of the last added element (`Au.wpfBuilder.Last`), which must be a `System.Windows.Controls.Decorator` (for example `System.Windows.Controls.Border` or `System.Windows.Documents.AdornerDecorator`) or `System.Windows.Controls.ContentControl` (for example `System.Windows.Controls.Button`).

##### Returns

`Au.wpfBuilder`

#### Remarks

For added elements call `Au.wpfBuilder.Dock`, maybe except for the last element that fills remaining space.

* * *

## Overload 2

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child `System.Windows.Controls.DockPanel` panel that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartDock<T>(object header) where T : HeaderedContentControl, new()
```

##### Parameters

- *header*  (`object`):
    Header text/content.

##### Returns

`Au.wpfBuilder`

##### Type Parameters

- `T`

* * *

## Overload 3

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child `System.Windows.Controls.DockPanel` panel that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartDock<T>(out T container, object header) where T : HeaderedContentControl, new()
```

##### Parameters

- *container*  (`T`):
    Receives the content control's variable. The function creates new control of the type.
- *header*  (`object`):
    Header text/content.

##### Returns

`Au.wpfBuilder`

##### Type Parameters

- `T`