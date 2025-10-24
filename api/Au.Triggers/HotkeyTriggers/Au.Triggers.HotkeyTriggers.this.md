# Indexer of `Au.Triggers.HotkeyTriggers`

## Overload 1

Adds a hotkey trigger.

```
public Action<HotkeyTriggerArgs> this[string hotkey, TKFlags flags = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *hotkey*  (`string`):
    A hotkey, like with `Au.keys.send`. See [key names and operators](../articles/Key%20names%20and%20operators.html). Can contain 0 to 4 modifier keys (`Ctrl`, `Shift`, `Alt`, `Win`) and 1 non-modifier key. Examples: `"F11"`, `"Ctrl+K"`, `"Ctrl+Shift+Alt+Win+A"`. To ignore modifiers: `"?+K"`. Then the trigger works with any combination of modifiers. To ignore a modifier: `"Ctrl?+K"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?+K"`, `"Ctrl+Shift?+K"`.
- *flags*  (`Au.Triggers.TKFlags`)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Exceptions

- `ArgumentException`:
    Invalid hotkey string or flags.
- `InvalidOperationException`:
    Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.HotkeyTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.

* * *

## Overload 2

Adds a hotkey trigger.

```
public Action<HotkeyTriggerArgs> this[KKey key, string modKeys, TKFlags flags = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *key*  (`Au.Types.KKey`)
- *modKeys*  (`string`):
    Modifier keys. See [key names and operators](../articles/Key%20names%20and%20operators.html). Examples: `"Ctrl"`, `"Ctrl+Shift+Alt+Win"`. To ignore modifiers: `"?"`. Then the trigger works with any combination of modifiers. To ignore a modifier: `"Ctrl?"`. Then the trigger works with or without the modifier. More examples: `"Ctrl?+Shift?"`, `"Ctrl+Shift?"`.
- *flags*  (`Au.Triggers.TKFlags`)
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

`Action<Au.Triggers.HotkeyTriggerArgs>`