# Method `Au.More.StringUtil.FlagsFromLetters`

Parses flags from string where flags are mapped to characters. See `Au.More.StringUtil.FlagsToLetters`

```
public static int FlagsFromLetters(string s, params (int flag, char c)[] map)
```

##### Parameters

- *s*  (`string`)
- *map*  (`(int flag, char c)[]`)

##### Returns

`int`

#### Remarks

If the string is a number, interprets it as the flags value. Don't use ASCII digits for flags. Any other characters are OK, not only letters.