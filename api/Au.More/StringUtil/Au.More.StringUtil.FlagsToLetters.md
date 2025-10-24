# Method `Au.More.StringUtil.FlagsToLetters`

Converts flags to string where flags are mapped to characters.

```
public static string FlagsToLetters(int flags, params (int flag, char c)[] map)
```

##### Parameters

- *flags*  (`int`)
- *map*  (`(int flag, char c)[]`)

##### Returns

`string`

#### Remarks

Don't use ASCII digits for flags, because `Au.More.StringUtil.FlagsFromLetters` interprets a number-string as the flags value. Any other characters are OK, not only letters.