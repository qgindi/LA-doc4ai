# Method `Au.Types.ExtWpf.UiaClick`

Calls `System.Windows.Automation.Provider.IInvokeProvider.Invoke`, which sends a request to click the button. Note: it's async; more info in Remarks.

```
public static void UiaClick(this Button t)
```

##### Parameters

- *t*  (`Button`)

##### Exceptions

- `ElementNotEnabledException`

#### Remarks

It is async (does not wait until finished). The button click event is raised after this function returns.

Does not click if the button is disabled.

Another way: `button.RaiseEvent(new RoutedEventArgs(Button.ClickEvent));`. It is sync, ignores disabled state, and ignores `System.Windows.Controls.Primitives.ButtonBase.Command`.