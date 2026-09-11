# Indexer of `Au.Triggers.MouseTriggers`

## Overload 1

Adds a mouse click trigger.

```csharp
public Action<MouseTriggerArgs> this[TMClick button, string modKeys = null, TMFlags flags = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *button*  (`Au.Triggers.TMClick`):
  Enum: Left, Right, Middle, X1, X2.
- *modKeys*  (`string`):
  Modifier keys. See [key names and operators](🔗).
  Examples:`"Ctrl"`, `"Ctrl+Shift+Alt+Win"`.
  To ignore modifiers:`"?"`. Then the trigger works with any combination of modifiers.
  To ignore a modifier:`"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`):
  Enum: ShareEvent, ButtonModUp, LeftMod, RightMod.
- *f_*  (`string`):
  [Caller info parameter](🔗)
- *l_*  (`int`):
  [Caller info parameter](🔗)

##### Exceptions

- `ArgumentException`:
  Invalid *modKeys* string or *flags*.
- `InvalidOperationException`:
  Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.MouseTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.

* * *

## Overload 2

Adds a mouse wheel trigger.

```csharp
public Action<MouseTriggerArgs> this[TMWheel direction, string modKeys = null, TMFlags flags = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *direction*  (`Au.Triggers.TMWheel`):
  Enum: Forward, Backward, Left, Right.
- *modKeys*  (`string`):
  Modifier keys. See [key names and operators](🔗).
  Examples:`"Ctrl"`, `"Ctrl+Shift+Alt+Win"`.
  To ignore modifiers:`"?"`. Then the trigger works with any combination of modifiers.
  To ignore a modifier:`"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`):
  Enum: ShareEvent, ButtonModUp, LeftMod, RightMod.
- *f_*  (`string`):
  [Caller info parameter](🔗)
- *l_*  (`int`):
  [Caller info parameter](🔗)

##### Exceptions

- `ArgumentException`:
  Invalid *modKeys* string or *flags*.
- `InvalidOperationException`:
  Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.MouseTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.

* * *

## Overload 3

Adds a mouse screen edge trigger.

```csharp
public Action<MouseTriggerArgs> this[TMEdge edge, string modKeys = null, TMFlags flags = 0, screen screen = default, string f_ = null, int l_ = 0, string a1_ = null] { set; }
```

##### Parameters

- *edge*  (`Au.Triggers.TMEdge`):
  Enum: Top, TopInCenter50, TopInLeft25, TopInRight25, Bottom, BottomInCenter50, BottomInLeft25, BottomInRight25, Left, LeftInCenter50, LeftInTop25, LeftInBottom25, Right, RightInCenter50, RightInTop25, RightInBottom25.
- *modKeys*  (`string`):
  Modifier keys. See [key names and operators](🔗).
  Examples:`"Ctrl"`, `"Ctrl+Shift+Alt+Win"`.
  To ignore modifiers:`"?"`. Then the trigger works with any combination of modifiers.
  To ignore a modifier:`"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`):
  Enum: ShareEvent, ButtonModUp, LeftMod, RightMod.
- *screen*  (`Au.screen`):
  The trigger will work in this screen (display monitor). Default: the primary screen.
  Should be lazy or default; else the function calls`Au.print.warning`.
  Examples:`screen.at.left(true)`, `screen.index(1, true)`.
  If`screen.ofMouse`, the trigger will work in any screen.
- *f_*  (`string`):
  [Caller info parameter](🔗)
- *l_*  (`int`):
  [Caller info parameter](🔗)
- *a1_*  (`string`):
  [Caller info parameter](🔗)

##### Exceptions

- `ArgumentException`:
  Invalid *modKeys* string or *flags*.
- `InvalidOperationException`:
  Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.MouseTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.

* * *

## Overload 4

Adds a mouse move trigger.

```csharp
public Action<MouseTriggerArgs> this[TMMove move, string modKeys = null, TMFlags flags = 0, screen screen = default, string f_ = null, int l_ = 0, string a1_ = null] { set; }
```

##### Parameters

- *move*  (`Au.Triggers.TMMove`):
  Enum: RightLeft, RightLeftInCenter50, RightLeftInTop25, RightLeftInBottom25, LeftRight, LeftRightInCenter50, LeftRightInTop25, LeftRightInBottom25, UpDown, UpDownInCenter50, UpDownInLeft25, UpDownInRight25, DownUp, DownUpInCenter50, DownUpInLeft25, DownUpInRight25.
- *modKeys*  (`string`):
  Modifier keys. See [key names and operators](🔗).
  Examples:`"Ctrl"`, `"Ctrl+Shift+Alt+Win"`.
  To ignore modifiers:`"?"`. Then the trigger works with any combination of modifiers.
  To ignore a modifier:`"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`):
  Enum: ShareEvent, ButtonModUp, LeftMod, RightMod.
- *screen*  (`Au.screen`):
  The trigger will work in this screen (display monitor). Default: the primary screen.
  Should be lazy or default; else the function calls`Au.print.warning`.
  Examples:`screen.at.left(true)`, `screen.index(1, true)`.
  If`screen.ofMouse`, the trigger will work in any screen.
- *f_*  (`string`):
  [Caller info parameter](🔗)
- *l_*  (`int`):
  [Caller info parameter](🔗)
- *a1_*  (`string`):
  [Caller info parameter](🔗)

##### Exceptions

- `ArgumentException`:
  Invalid *modKeys* string or *flags*.
- `InvalidOperationException`:
  Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.MouseTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.