# Method `Au.wpfBuilder.Add`

## Overload 1

Adds an existing element.

```
public wpfBuilder Add(FrameworkElement element, bool raw = false)
```

##### Parameters

- *element*  (`FrameworkElement`)
- *raw*  (`bool`):
    Don't change element properties, except margin. If `false` (default), works like other `Add` overloads: for some element types sets padding, alignment, properties specified in `Au.wpfBuilder.Options`, etc.

##### Returns

`Au.wpfBuilder`

### See Also

`Au.wpfBuilder.And`

`Au.wpfBuilder.Child`

`Au.wpfBuilder.Options`

`Au.wpfBuilder.AlsoAll`

* * *

## Overload 2

Creates and adds element of type *T* (control etc of any type).

```
public wpfBuilder Add<T>(out T variable, object text = null) where T : FrameworkElement, new()
```

##### Parameters

- *variable*  (`T`):
    Receives element's variable. The function creates element of variable's type. You can use the variable to set element's properties before showing window or/and to get value after. Examples: `.Add(out CheckBox c1, "Text")`, `.Add(out _textBox1)`. If don't need a variable: `.Add(out Label _, "Text")` or `.Add<Label>("Text")`.
- *text*  (`object`):

    Text, header or other content. Supported element types (or base types):

    - `System.Windows.Controls.TextBox` - sets `Text` property.
    - `System.Windows.Controls.ComboBox` - sets `Text` property (see also `Au.wpfBuilder.Items`).
    - `System.Windows.Controls.PasswordBox` - sets `Password` property.
    - `System.Windows.Controls.TextBlock` - sets `Text` property (see also `Au.wpfBuilder.FormatText` and `Au.wpfBuilder.formattedText`).
    - `System.Windows.Controls.HeaderedContentControl`, `System.Windows.Controls.HeaderedItemsControl` - sets `Header` property (see also `Au.wpfBuilder.FormatText` and `Au.wpfBuilder.formattedText`).
    - `System.Windows.Controls.ContentControl` - sets `Content` property (can be string, other element, etc) (see also `Au.wpfBuilder.FormatText` and `Au.wpfBuilder.formattedText`).
    - `System.Windows.Controls.RichTextBox` - calls `AppendText` (see also `Au.wpfBuilder.LoadFile`).
    - Other element types that have `Text` property.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The function does not support non-`null` *text* for this element type.

##### Type Parameters

- `T`

### See Also

`Au.wpfBuilder.And`

`Au.wpfBuilder.Child`

`Au.wpfBuilder.Options`

`Au.wpfBuilder.AlsoAll`

* * *

## Overload 3

Creates and adds element of type *T* (any type). This overload can be used when don't need element's variable.

```
public wpfBuilder Add<T>(object text = null) where T : FrameworkElement, new()
```

##### Parameters

- *text*  (`object`):
    Text, header or other content. More info - see other overload.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The function does not support non-`null` *text* for this element type.

##### Type Parameters

- `T`

### See Also

`Au.wpfBuilder.And`

`Au.wpfBuilder.Child`

`Au.wpfBuilder.Options`

`Au.wpfBuilder.AlsoAll`

* * *

## Overload 4

Adds 2 elements: `System.Windows.Controls.Label` and element of type *T* (control etc of any type).

```
public wpfBuilder Add<T>(object label, out T variable, object text = null, WBGridLength? row2 = null) where T : FrameworkElement, new()
```

##### Parameters

- *label*  (`object`):
    Label text. Usually string or `System.Windows.Controls.TextBlock`. Example: `new TextBlock() { TextWrapping = TextWrapping.Wrap, Text = "long text" }`.
- *variable*  (`T`):
    Variable of second element. More info - see other overload.
- *text*  (`object`):
    Text, header or other content of second element. More info - see other overload.
- *row2*  (`Au.Types.WBGridLength?`):
    If not `null`, after adding first element calls `Au.wpfBuilder.Row` with this argument.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    If the function does not support non-`null` *text* for this element type.

##### Type Parameters

- `T`

#### Remarks

Finally calls `Au.wpfBuilder.LabeledBy`; it sets `System.Windows.Controls.Label.Target`, calls `System.Windows.Automation.AutomationProperties.SetLabeledBy` and applies the *bindLabelVisibility* option (see `Au.wpfBuilder.Options`).

* * *

## Overload 5

Adds 2 elements: `System.Windows.Controls.Label` and an existing element (control etc of any type).

```
public wpfBuilder Add(object label, FrameworkElement element, WBGridLength? row2 = null)
```

##### Parameters

- *label*  (`object`):
    Label text. Usually string or `System.Windows.Controls.TextBlock`. Example: `new TextBlock() { TextWrapping = TextWrapping.Wrap, Text = "long text" }`.
- *element*  (`FrameworkElement`)
- *row2*  (`Au.Types.WBGridLength?`):
    If not `null`, after adding first element calls `Au.wpfBuilder.Row` with this argument.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    If the function does not support non-`null` *text* for this element type.

#### Remarks

Finally calls `Au.wpfBuilder.LabeledBy`; it sets `System.Windows.Controls.Label.Target`, calls `System.Windows.Automation.AutomationProperties.SetLabeledBy` and applies the *bindLabelVisibility* option (see `Au.wpfBuilder.Options`).