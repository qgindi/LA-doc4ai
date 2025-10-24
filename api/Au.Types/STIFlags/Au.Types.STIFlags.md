# Enum `Au.Types.STIFlags`

Flags for `Au.Types.ExtString.ToInt` and similar functions.

```
[Flags]
public enum STIFlags
```

### Fields

| Name | Description |
| --- | --- |
| DontSkipSpaces | Fail if string starts with a whitespace character. |
| IsHexWithout0x | The number in string is hexadecimal without a prefix, like `"1A"`. |
| NoHex | Don't support hexadecimal numbers (numbers with prefix `"0x"`). |