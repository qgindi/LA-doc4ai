# Method `Au.wpfBuilder.StartStack`

## Overload 1

Adds `System.Windows.Controls.StackPanel` panel that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartStack(bool vertical = false, bool childOfLast = false)
```

##### Parameters

- *vertical*  (`bool`)
- *childOfLast*  (`bool`):
    Add as a child or content of the last added element (`Au.wpfBuilder.Last`), which must be a `System.Windows.Controls.Decorator` (for example `System.Windows.Controls.Border` or `System.Windows.Documents.AdornerDecorator`) or `System.Windows.Controls.ContentControl` (for example `System.Windows.Controls.Button`).

##### Returns

`Au.wpfBuilder`

* * *

## Overload 2

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child `System.Windows.Controls.StackPanel` panel that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartStack<T>(object header, bool vertical = false) where T : HeaderedContentControl, new()
```

##### Parameters

- *header*  (`object`):
    Header text/content.
- *vertical*  (`bool`)

##### Returns

`Au.wpfBuilder`

##### Type Parameters

- `T`

* * *

## Overload 3

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child `System.Windows.Controls.StackPanel` panel that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartStack<T>(out T container, object header, bool vertical = false) where T : HeaderedContentControl, new()
```

##### Parameters

- *container*  (`T`):
    Receives the content control's variable. The function creates new control of the type.
- *header*  (`object`):
    Header text/content.
- *vertical*  (`bool`)

##### Returns

`Au.wpfBuilder`

##### Type Parameters

- `T`