# Method `Au.Types.ExtString.Escape`

Replaces unsafe characters with C# escape sequences. If the string contains these characters, replaces and returns new string. Else returns this string.

```
public static string Escape(this string t, int limit = 0, bool quote = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *limit*  (`int`):
    If the final string is longer than *limit*, get its substring 0 to *limit*-1 with appended `'…'` character. The enclosing `""` are not counted.
- *quote*  (`bool`):
    Enclose in `""`.

##### Returns

`string`

#### Remarks

Replaces these characters: `'\\'`, `'"'`, `'\t'`, `'\n'`, `'\r'` and all in range 0-31.