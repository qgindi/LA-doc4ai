# Property `Au.wnd.NameWinforms`

Gets the `System.Windows.Forms.Control.Name` property value of a .NET Windows Forms control.

```
public string NameWinforms { get; }
```

##### Property Value

`string`

`null` if it is not a Windows Forms control or if failed.

#### Remarks

> **Note:**
> Use this with controls of other processes. Don't use with your controls, when you have a `Control` object.

> **Note:**
> Slow when getting names of multiple controls in a window. Instead create a `Au.More.WinformsControlNames` instance and call its `Au.More.WinformsControlNames.GetControlName` method for each control.

### See Also

`Au.More.WinformsControlNames.IsWinformsControl`