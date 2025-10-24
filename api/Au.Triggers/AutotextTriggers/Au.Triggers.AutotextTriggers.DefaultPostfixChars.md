# Property `Au.Triggers.AutotextTriggers.DefaultPostfixChars`

Default value for the *postfixChars* parameter used for triggers added afterwards. Default: `null`.

```
public string DefaultPostfixChars { get; set; }
```

##### Exceptions

- `ArgumentException`:
    The value contains letters or digits.

##### Property Value

`string`

#### Remarks

If `null` (default), postfix characters are all except alpha-numeric (see `char.IsLetterOrDigit`). The value cannot contain alpha-numeric characters (exception) and `Au.Triggers.AutotextTriggers.WordCharsPlus` characters (triggers will not work). For `Enter` use `'\r'`.