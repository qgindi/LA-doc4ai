# Method `Au.More.WinformsControlNames.GetSingleControlName`

Gets the programming name of a Windows Forms control.

```
public static string GetSingleControlName(wnd c)
```

##### Parameters

- *c*  (`Au.wnd`):
    The control. Can be top-level window too.

##### Returns

`string`

`null` if it is not a Windows Forms control or if failed.

#### Remarks

This function is easy to use and does not throw exceptions. However, when you need names of multiple controls of a single window, better create a `Au.More.WinformsControlNames` instance (once) and for each control call its `GetControlName` method, it will be faster.