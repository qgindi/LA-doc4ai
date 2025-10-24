# Method `Au.wpfBuilder.LabeledBy`

## Overload 1

Makes an element behave as a label of the last added element (`Au.wpfBuilder.Last`).

```
public wpfBuilder LabeledBy(FrameworkElement label, bool? bindVisibility = null)
```

##### Parameters

- *label*  (`FrameworkElement`):
    The label element. Usually `System.Windows.Controls.Label` or `System.Windows.Controls.TextBlock`, but can be any element.
- *bindVisibility*  (`bool?`):
    If `true`, binds `Visibility` of *label* to that of the labeled element. If `false`, does not bind. If `null` (default), binds if the *bindLabelVisibility* option is true (see `Au.wpfBuilder.Options`). If binds `Visibility`, also binds `IsEnabled` if *label* is `System.Windows.Controls.Label` or `System.Windows.Controls.TextBlock`.

##### Returns

`Au.wpfBuilder`

#### Remarks

Sets *label*'s `System.Windows.Controls.Label.Target` if it's `System.Windows.Controls.Label`. Calls `System.Windows.Automation.AutomationProperties.SetLabeledBy`.

* * *

## Overload 2

Makes `Au.wpfBuilder.Last2` behave as a label of `Au.wpfBuilder.Last`.

```
public wpfBuilder LabeledBy(bool? bindVisibility = null)
```

##### Parameters

- *bindVisibility*  (`bool?`):
    If `true`, binds `Visibility` of *label* to that of the labeled element. If `false`, does not bind. If `null` (default), binds if the *bindLabelVisibility* option is true (see `Au.wpfBuilder.Options`). If binds `Visibility`, also binds `IsEnabled` if *label* is `System.Windows.Controls.Label` or `System.Windows.Controls.TextBlock`.

##### Returns

`Au.wpfBuilder`

#### Remarks

Sets *label*'s `System.Windows.Controls.Label.Target` if it's `System.Windows.Controls.Label`. Calls `System.Windows.Automation.AutomationProperties.SetLabeledBy`.