# Enum `Au.Triggers.TAFlags`

Flags of autotext triggers.

```
[Flags]
public enum TAFlags : byte
```

##### Remarks

To avoid passing flags to each trigger as the *flags* parameter, use `Au.Triggers.AutotextTriggers.DefaultFlags`; its initial value is 0, which means: case-insensitive, erase the typed text with `Backspace`, modify the replacement text depending on the case of the typed text.

### Fields

| Name | Description |
| --- | --- |
| Confirm | Let `Au.Triggers.AutotextTriggerArgs.Replace` call `Au.Triggers.AutotextTriggerArgs.Confirm` and do nothing if it returns `false`. |
| DontErase | Let `Au.Triggers.AutotextTriggerArgs.Replace` don't erase the user-typed text. Without this flag it erases text with the `Backspace` key or selects with `Shift+Left`. If `Replace` not called, text is not erased/selected regardless of this flag. |
| MatchCase | Case-sensitive. |
| RemovePostfix | Let `Au.Triggers.AutotextTriggerArgs.Replace` remove the postfix delimiter character. |
| ReplaceRaw | (see section `details1` in Footnotes) |
| ShiftLeft | Let `Au.Triggers.AutotextTriggerArgs.Replace` select text with `Shift+Left` instead of erasing with `Backspace`. Except in console windows. See also `Au.Triggers.AutotextTriggerArgs.ShiftLeft`. |

## Footnotes

###### details1

Let `Au.Triggers.AutotextTriggerArgs.Replace` don't modify the replacement text. 
Without `ReplaceRaw` or `MatchCase` it:

- If the first character of the typed text is uppercase, makes the first character of the replacement text uppercase.
- If all typed text is uppercase, makes the replacement text uppercase.