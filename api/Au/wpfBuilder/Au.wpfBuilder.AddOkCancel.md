# Method `Au.wpfBuilder.AddOkCancel`

## Overload 1

Adds **OK** and/or **Cancel** and/or **Apply** buttons.

```
public wpfBuilder AddOkCancel(string ok = "OK", string cancel = "Cancel", string apply = null, bool? stackPanel = null)
```

##### Parameters

- *ok*  (`string`):
    Text of **OK** button. If `null`, does not add the button.
- *cancel*  (`string`):
    Text of **Cancel** button. If `null`, does not add the button.
- *apply*  (`string`):
    Text of **Apply** button. If `null`, does not add the button.
- *stackPanel*  (`bool?`):
    Add a right-bottom aligned `System.Windows.Controls.StackPanel` that contains the buttons. See `Au.wpfBuilder.StartOkCancel`. If `null` (default), adds if not already in a stack panel, except when there is 1 button.

##### Returns

`Au.wpfBuilder`

#### Remarks

Sets properties of **OK**/**Cancel** buttons so that click and `Enter`/`Esc` close the window; then `Au.wpfBuilder.ShowDialog` returns `true` on **OK**, `false` on **Cancel**. See also event `Au.wpfBuilder.OkApply`.

* * *

## Overload 2

Adds **OK** and/or **Cancel** and/or **Apply** buttons.

```
public wpfBuilder AddOkCancel(out Button bOK, out Button bCancel, out Button bApply, string ok = "OK", string cancel = "Cancel", string apply = null, bool? stackPanel = null)
```

##### Parameters

- *bOK*  (`Button`):
    Variable of **OK** button.
- *bCancel*  (`Button`):
    Variable of **Cancel** button.
- *bApply*  (`Button`):
    Variable of **Apply** button.
- *ok*  (`string`):
    Text of **OK** button. If `null`, does not add the button.
- *cancel*  (`string`):
    Text of **Cancel** button. If `null`, does not add the button.
- *apply*  (`string`):
    Text of **Apply** button. If `null`, does not add the button.
- *stackPanel*  (`bool?`):
    Add a right-bottom aligned `System.Windows.Controls.StackPanel` that contains the buttons. See `Au.wpfBuilder.StartOkCancel`. If `null` (default), adds if not already in a stack panel, except when there is 1 button.

##### Returns

`Au.wpfBuilder`

#### Remarks

Sets properties of **OK**/**Cancel** buttons so that click and `Enter`/`Esc` close the window; then `Au.wpfBuilder.ShowDialog` returns `true` on **OK**, `false` on **Cancel**. See also event `Au.wpfBuilder.OkApply`.