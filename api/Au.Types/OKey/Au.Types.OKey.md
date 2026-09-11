# Class `Au.Types.OKey`

Options for functions of class `Au.keys`.
Some options also are used with`Au.clipboard` functions that send keys (`Ctrl+V` etc).

```csharp
public sealed class OKey
```

##### Examples

```csharp
opt.key.KeySpeed = 50;
```

Set options for trigger actions.

```csharp
Triggers.Options.BeforeAction = o => { opt.key.KeySpeed = 50; };
```

##### Inheritance

`object` → `OKey`

### Constructors

`OKey(OKey)`

### Properties

`Hook`, `KeySpeed`, `KeySpeedClipboard`, `NoBlockInput`, `NoCapsOff`, `NoModOff`, `PasteLength`, `PasteSleep`, `PasteWorkaround`, `RestoreClipboard`, `RestoreClipboardAllFormats`, `RestoreClipboardExceptFormats`, `SleepFinally`, `TextHow`, `TextShiftEnter`, `TextSpeed`

### Methods

`PrintClipboard`, `ToString`

### See Also

`Au.opt.key`