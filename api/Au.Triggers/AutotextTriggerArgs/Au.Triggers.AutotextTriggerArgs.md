# Class `Au.Triggers.AutotextTriggerArgs`

Arguments for actions of autotext triggers. You can use functions `Au.Triggers.AutotextTriggerArgs.Replace` and `Au.Triggers.AutotextTriggerArgs.Menu` to replace user-typed text.

```
public class AutotextTriggerArgs : TriggerArgs
```

##### Inheritance

`object` → `Au.Triggers.TriggerArgs` → `AutotextTriggerArgs`

### Constructors

`AutotextTriggerArgs(AutotextTrigger, wnd, string, bool)`

### Properties

`HasPostfixChar`, `ShiftLeft`, `Text`, `Trigger`, `Window`

### Methods

`Confirm`, `Menu`, `Replace`, `Replace2`, `SendPostfix`, `ToString`

### Members inherited from other types of this library
`TriggerArgs.TriggerBase`, `TriggerArgs.DisableTriggerUntilClosed()`