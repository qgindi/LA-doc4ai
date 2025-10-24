# Property `Au.uacInfo.IsUIAccess`

Returns `true` if the process has [UAC](../articles/UAC.html) uiAccess property. A uiAccess process can access/automate all windows of processes running in the same user session.

```
public bool IsUIAccess { get; }
```

##### Property Value

`bool`

#### Remarks

Most processes don't have this property. They cannot access/automate windows of higher integrity level (High, System, uiAccess) processes and Windows 8 store apps. For example, cannot send keys and Windows messages. Note: High IL (admin) processes also can have this property, therefore `IsUIAccess` is not the same as `IntegrityLevel==IL.UIAccess` (`Au.uacInfo.IntegrityLevel` returns `UIAccess` only for Medium+uiAccess processes; for High+uiAccess processes it returns `High`). Some Windows API work slightly differently with uiAccess and non-uiAccess admin processes. This property is rarely useful. Instead use other properties of this class.