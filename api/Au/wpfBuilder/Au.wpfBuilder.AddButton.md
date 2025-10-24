# Method `Au.wpfBuilder.AddButton`

## Overload 1

Adds button with `System.Windows.Controls.Primitives.ButtonBase.Click` event handler.

```
public wpfBuilder AddButton(out Button variable, object text, Action<WBButtonClickArgs> click, WBBFlags flags = 0)
```

##### Parameters

- *variable*  (`Button`):
    Receives button's variable.
- *text*  (`object`):
    Text/content (`System.Windows.Controls.ContentControl.Content`).
- *click*  (`Action<Au.Types.WBButtonClickArgs>`):
    Action to call when the button clicked. Its parameter's property `Cancel` can be used to prevent closing the window when clicked this **OK** button. Not called if validation fails.
- *flags*  (`Au.Types.WBBFlags`)

##### Returns

`Au.wpfBuilder`

#### Remarks

If *flags* contains `OK` or `Apply` or `Validate` and this window contains elements for which was called `Au.wpfBuilder.Validation`, on click performs validation; if fails, does not call the *click* action and does not close the window.

* * *

## Overload 2

Adds button with `System.Windows.Controls.Primitives.ButtonBase.Click` event handler.

```
public wpfBuilder AddButton(object text, Action<WBButtonClickArgs> click, WBBFlags flags = 0)
```

##### Parameters

- *text*  (`object`):
    Text/content (`System.Windows.Controls.ContentControl.Content`).
- *click*  (`Action<Au.Types.WBButtonClickArgs>`):
    Action to call when the button clicked. Its parameter's property `Cancel` can be used to prevent closing the window when clicked this **OK** button. Not called if validation fails.
- *flags*  (`Au.Types.WBBFlags`)

##### Returns

`Au.wpfBuilder`

#### Remarks

If *flags* contains `OK` or `Apply` or `Validate` and this window contains elements for which was called `Au.wpfBuilder.Validation`, on click performs validation; if fails, does not call the *click* action and does not close the window.

* * *

## Overload 3

Adds button that closes the window and sets `Au.wpfBuilder.ResultButton`.

```
public wpfBuilder AddButton(object text, int result)
```

##### Parameters

- *text*  (`object`):
    Text/content (`System.Windows.Controls.ContentControl.Content`).
- *result*  (`int`):
    `Au.wpfBuilder.ResultButton` value when clicked this button.

##### Returns

`Au.wpfBuilder`

#### Remarks

When clicked, sets `Au.wpfBuilder.ResultButton` = *result*, closes the window, and `Au.wpfBuilder.ShowDialog` returns `true`.