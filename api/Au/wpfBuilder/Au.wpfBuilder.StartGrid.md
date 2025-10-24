# Method `Au.wpfBuilder.StartGrid`

## Overload 1

Adds `System.Windows.Controls.Grid` panel (table) that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartGrid(bool childOfLast = false)
```

##### Parameters

- *childOfLast*  (`bool`):
    Add as a child or content of the last added element (`Au.wpfBuilder.Last`), which must be a `System.Windows.Controls.Decorator` (for example `System.Windows.Controls.Border` or `System.Windows.Documents.AdornerDecorator`) or `System.Windows.Controls.ContentControl` (for example `System.Windows.Controls.Button`).

##### Returns

`Au.wpfBuilder`

#### Remarks

How `Au.wpfBuilder.Last` changes: after calling this function it is the grid (`Au.wpfBuilder.Panel`); after adding an element it is the element; finally, after calling `Au.wpfBuilder.End` it is the grid if *childOfLast* `false`, else its parent. The same with all `StartX` functions.

* * *

## Overload 2

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child `System.Windows.Controls.Grid` panel (table) that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartGrid<T>(object header) where T : HeaderedContentControl, new()
```

##### Parameters

- *header*  (`object`):
    Header text/content.

##### Returns

`Au.wpfBuilder`

##### Type Parameters

- `T`

#### Remarks

How `Au.wpfBuilder.Last` changes: after calling this function it is the grid (`Au.wpfBuilder.Panel`); after adding an element it is the element; finally, after calling `Au.wpfBuilder.End` it is the content control (grid's parent). The same with all `StartX` functions.

#### Examples

```
b.StartGrid<GroupBox>("Group");
```

* * *

## Overload 3

Adds a headered content control (`System.Windows.Controls.GroupBox`, `System.Windows.Controls.Expander`, etc) with child `System.Windows.Controls.Grid` panel (table) that will contain elements added with `Au.wpfBuilder.Add` etc. Finally call `Au.wpfBuilder.End` to return to current panel.

```
public wpfBuilder StartGrid<T>(out T container, object header) where T : HeaderedContentControl, new()
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

#### Remarks

How `Au.wpfBuilder.Last` changes: after calling this function it is the grid (`Au.wpfBuilder.Panel`); after adding an element it is the element; finally, after calling `Au.wpfBuilder.End` it is the content control (grid's parent). The same with all `StartX` functions.

#### Examples

```
b.StartGrid(out Expander g, "Expander"); g.IsExpanded=true;
```