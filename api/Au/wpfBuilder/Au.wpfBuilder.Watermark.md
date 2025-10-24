# Method `Au.wpfBuilder.Watermark`

## Overload 1

Sets watermark/hint/cue text of the last added `System.Windows.Controls.TextBox`, `System.Windows.Controls.PasswordBox` or editable `System.Windows.Controls.ComboBox` control. The text is visible only when the control text is empty.

```
public wpfBuilder Watermark(string text)
```

##### Parameters

- *text*  (`string`):
    Watermark text.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element isn't `System.Windows.Controls.TextBox`, `System.Windows.Controls.PasswordBox` or editable `System.Windows.Controls.ComboBox` control.

#### Remarks

In some kinds of windows it may not work unless a parent or ancestor of the control is an `System.Windows.Documents.AdornerDecorator` (like in the example).

#### Examples

```
b.R.Add<AdornerDecorator>().Child().Add(out TextBox text1).Watermark("Water");
```

More examples in Cookbook.

* * *

## Overload 2

Sets watermark/hint/cue text of the last added `System.Windows.Controls.TextBox`, `System.Windows.Controls.PasswordBox` or editable `System.Windows.Controls.ComboBox` control. The text is visible only when the control text is empty.

```
public wpfBuilder Watermark(out WatermarkAdorner adorner, string text)
```

##### Parameters

- *adorner*  (`Au.More.WatermarkAdorner`):
    Receives the adorner. It can be used to change watermark text later.
- *text*  (`string`):
    Watermark text.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element isn't `System.Windows.Controls.TextBox`, `System.Windows.Controls.PasswordBox` or editable `System.Windows.Controls.ComboBox` control.

#### Remarks

In some kinds of windows it may not work unless a parent or ancestor of the control is an `System.Windows.Documents.AdornerDecorator` (like in the example).

#### Examples

```
b.R.Add<AdornerDecorator>().Child().Add(out TextBox text1).Watermark("Water");
```

More examples in Cookbook.