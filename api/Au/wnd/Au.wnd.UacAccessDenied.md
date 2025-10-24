# Property `Au.wnd.UacAccessDenied`

Returns `true` if [UAC](../articles/UAC.html) would not allow to automate the window. It happens when current process has lower UAC integrity level and is not uiAccess, unless UAC is turned off.

```
public bool UacAccessDenied { get; }
```

##### Property Value

`bool`

#### Remarks

Supports `Au.lastError`.