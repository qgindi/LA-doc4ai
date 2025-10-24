# Class `Au.More.WinformsControlNames`

Gets programming names of .NET Windows Forms controls.

```
public sealed class WinformsControlNames : IDisposable
```

##### Remarks

Usually each control has a unique name. It's the `System.Windows.Forms.Control.Name` property. Useful to identify controls without a classic name/text. The control id of these controls is not useful, it is not constant.

##### Inheritance

`object` → `WinformsControlNames`

### Constructors

`WinformsControlNames(wnd)`

### Methods

`Dispose`, `GetControlName`, `GetSingleControlName`, `IsWinformsControl`