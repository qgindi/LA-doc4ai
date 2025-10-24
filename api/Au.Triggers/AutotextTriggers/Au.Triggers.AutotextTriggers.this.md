# Indexer of `Au.Triggers.AutotextTriggers`

Adds an autotext trigger.

```
public Action<AutotextTriggerArgs> this[string text, TAFlags? flags = null, TAPostfix? postfixType = null, string postfixChars = null, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *text*  (`string`):
    The action runs when the user types this text and a postfix character or key. By default case-insensitive.
- *flags*  (`Au.Triggers.TAFlags?`):
    Options. If omitted or `null`, uses `Au.Triggers.AutotextTriggers.DefaultFlags`. Some flags are used by `Au.Triggers.AutotextTriggerArgs.Replace`.
- *postfixType*  (`Au.Triggers.TAPostfix?`):
    Postfix type (character, key, any or none). If omitted or `null`, uses `Au.Triggers.AutotextTriggers.DefaultPostfixType`; default - a non-word character or the `Ctrl` key.
- *postfixChars*  (`string`):
    Postfix characters used when postfix type is `Char` or `CharOrKey` (default). If omitted or `null`, uses `Au.Triggers.AutotextTriggers.DefaultPostfixChars`; default - non-word characters.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Exceptions

- `ArgumentException`:

    - Text is empty or too long. Can be 1 - 100 characters.
    - Postfix characters contains letters or digits.
- `InvalidOperationException`:
    Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.AutotextTriggerArgs>`

#### Examples

See `Au.Triggers.ActionTriggers`.