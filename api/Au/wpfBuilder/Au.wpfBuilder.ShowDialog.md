# Method `Au.wpfBuilder.ShowDialog`

Shows the window and waits until closed.

```
public bool ShowDialog(DependencyObject owner = null)
```

##### Parameters

- *owner*  (`DependencyObject`):
    Owner window or element. Sets `System.Windows.Window.Owner`.

##### Returns

`bool`

##### Exceptions

- `InvalidOperationException`:

    - Container is not of type `Window`.
    - Missing `Au.wpfBuilder.End` for a panel added with a `StartX` function.

#### Remarks

Calls `Au.wpfBuilder.End`, sets `System.Windows.Window.Owner` and calls `System.Windows.Window.ShowDialog`. You can instead call these functions directly. Or call `System.Windows.Window.Show` to show as non-modal window, ie don't wait. Or add `Au.wpfBuilder.Panel` to some container window or other element, etc.