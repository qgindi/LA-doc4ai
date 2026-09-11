# Class `Au.Types.OMouse`

Options for functions of class `Au.mouse`.

```csharp
public sealed class OMouse
```

##### Remarks

Total `Click(x, y)` time is: mouse move + `Au.Types.OMouse.MoveSleepFinally` + button down + `Au.Types.OMouse.ClickSpeed` + button up + `Au.Types.OMouse.ClickSpeed` + `Au.Types.OMouse.ClickSleepFinally`.

##### Examples

```csharp
opt.mouse.MoveSpeed = 30;
```

##### Inheritance

`object` → `OMouse`

### Properties

`ClickSleepFinally`, `ClickSpeed`, `MoveSleepFinally`, `MoveSpeed`, `Relaxed`

### Methods

`ToString`

### See Also

`Au.opt.mouse`