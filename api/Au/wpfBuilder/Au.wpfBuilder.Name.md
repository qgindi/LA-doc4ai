# Method `Au.wpfBuilder.Name`

Sets `System.Windows.FrameworkElement.Name` of the last added element.

```
public wpfBuilder Name(string name, bool andUia = false)
```

##### Parameters

- *name*  (`string`):
    Name. Must start with a letter or `_`, and contain only letters, digits and `_`.
- *andUia*  (`bool`):
    Also set UI Automation name (`Au.wpfBuilder.UiaName`).

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `ArgumentException`:
    Invalid name.

#### Remarks

The `Name` property can be used to identify the element in code. It also sets the UIA `AutomationId` (regardless of *andUia*). It isn't displayed in UI.