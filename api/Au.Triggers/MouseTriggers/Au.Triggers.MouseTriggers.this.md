# Indexer of `Au.Triggers.MouseTriggers`

## Overload 1

Adds a mouse click trigger.

```
public Action<MouseTriggerArgs> this[TMClick button, string modKeys = null, TMFlags flags = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *button*  (`Au.Triggers.TMClick`)
- *modKeys*  (`string`):
    Modifier keys. See [key names and operators](../articles/Key%20names%20and%20operators.html). Examples: `"Ctrl"`, `"Ctrl+Shift+Alt+Win"`. To ignore modifiers: `"?"`. Then the trigger works with any combination of modifiers. To ignore a modifier: `"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

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

```
public Action<MouseTriggerArgs> this[TMWheel direction, string modKeys = null, TMFlags flags = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *direction*  (`Au.Triggers.TMWheel`)
- *modKeys*  (`string`):
    Modifier keys. See [key names and operators](../articles/Key%20names%20and%20operators.html). Examples: `"Ctrl"`, `"Ctrl+Shift+Alt+Win"`. To ignore modifiers: `"?"`. Then the trigger works with any combination of modifiers. To ignore a modifier: `"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

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

```
public Action<MouseTriggerArgs> this[TMEdge edge, string modKeys = null, TMFlags flags = 0, screen screen = default, string f_ = null, int l_ = 0, string a1_ = null] { set; }
```

##### Parameters

- *edge*  (`Au.Triggers.TMEdge`)
- *modKeys*  (`string`):
    Modifier keys. See [key names and operators](../articles/Key%20names%20and%20operators.html). Examples: `"Ctrl"`, `"Ctrl+Shift+Alt+Win"`. To ignore modifiers: `"?"`. Then the trigger works with any combination of modifiers. To ignore a modifier: `"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`)
- *screen*  (`Au.screen`):
    The trigger will work in this screen (display monitor). Default: the primary screen. Should be lazy or default; else the function calls `Au.print.warning`. Examples: `screen.at.left(true)`, `screen.index(1, true)`. If `screen.ofMouse`, the trigger will work in any screen.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *a1_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

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

```
public Action<MouseTriggerArgs> this[TMMove move, string modKeys = null, TMFlags flags = 0, screen screen = default, string f_ = null, int l_ = 0, string a1_ = null] { set; }
```

##### Parameters

- *move*  (`Au.Triggers.TMMove`)
- *modKeys*  (`string`):
    Modifier keys. See [key names and operators](../articles/Key%20names%20and%20operators.html). Examples: `"Ctrl"`, `"Ctrl+Shift+Alt+Win"`. To ignore modifiers: `"?"`. Then the trigger works with any combination of modifiers. To ignore a modifier: `"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TMFlags`)
- *screen*  (`Au.screen`):
    The trigger will work in this screen (display monitor). Default: the primary screen. Should be lazy or default; else the function calls `Au.print.warning`. Examples: `screen.at.left(true)`, `screen.index(1, true)`. If `screen.ofMouse`, the trigger will work in any screen.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *a1_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Exceptions

- `ArgumentException`:
    Invalid *modKeys* string or *flags*.
- `InvalidOperationException`:
    Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.MouseTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.