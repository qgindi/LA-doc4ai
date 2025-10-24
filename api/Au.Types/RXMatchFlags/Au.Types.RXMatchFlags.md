# Enum `Au.Types.RXMatchFlags`

Flags for `Au.regexp` class functions. Documented in PCRE help topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html).

```
[Flags]
public enum RXMatchFlags : uint
```

##### Remarks

These flags also exist in `Au.Types.RXFlags` (`Au.regexp` constructor flags). You can set them either when calling constructor or when calling other functions.

### Fields

| Name | Description |
| --- | --- |
| ANCHORED | Match only at the first position |
| ENDANCHORED | Pattern can match only at end of subject |
| NOTBOL | Subject string is not the beginning of a line |
| NOTEMPTY | An empty string is not a valid match |
| NOTEMPTY_ATSTART | An empty string at the start of the subject is not a valid match |
| NOTEOL | Subject string is not the end of a line |
| NO_UTF_CHECK | Do not check the subject for UTF validity |
| PARTIAL_HARD | Allow partial hard match. See `Au.Types.RXMatch.IsPartial`. |
| PARTIAL_SOFT | Allow partial soft match. See `Au.Types.RXMatch.IsPartial`. |