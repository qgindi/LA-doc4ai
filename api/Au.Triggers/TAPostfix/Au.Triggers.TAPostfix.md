# Enum `Au.Triggers.TAPostfix`

Postfix type of autotext triggers. The trigger action runs only when the user ends the autotext with a postfix character or key, unless postfix type is `None`. Default: `CharOrKey`.

```
public enum TAPostfix : byte
```

### Fields

| Name | Description |
| --- | --- |
| Char | A postfix character specified in the *postfixChars* parameter or `Au.Triggers.AutotextTriggers.DefaultPostfixChars` property. If not specified - any non-word character. |
| CharOrKey | A postfix character (see `Char`) or key (see `Key`). |
| Key | The `Ctrl` or `Shift` key. Default is `Ctrl`. You can change it with `Au.Triggers.AutotextTriggers.PostfixKey`. |
| None | Don't need a postfix. The action runs immediately when the user types the autotext. |