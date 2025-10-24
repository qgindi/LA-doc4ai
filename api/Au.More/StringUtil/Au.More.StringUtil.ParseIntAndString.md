# Method `Au.More.StringUtil.ParseIntAndString`

If string contains a number at *startIndex*, gets that number as `int`, also gets the string part that follows it, and returns `true`.

```
public static bool ParseIntAndString(string s, out int num, out string tail, int startIndex = 0, STIFlags flags = 0)
```

##### Parameters

- *s*  (`string`)
- *num*  (`int`):
    Receives the number. Receives 0 if no number.
- *tail*  (`string`):
    Receives the string part that follows the number, or `""`. Receives `null` if no number. Can be this variable.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

#### Remarks

For example, for string `"25text"` or `"25 text"` gets *num* = `25`, *tail* = `"text"`. Everything else is the same as with `Au.Types.ExtString.ToInt`.