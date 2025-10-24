# Method `Au.regexp.escapeQE`

Encloses string in `\Q \E` if it contains metacharacters `\^$.[|()?*+{` or if *always* == `true`.

```
public static string escapeQE(string s, bool always = false)
```

##### Parameters

- *s*  (`string`):
    Can be `null`.
- *always*  (`bool`):
    Enclose always, even if the string does not contain metacharacters. Should be `true` if the regular expression in which this string will be used has option "extended", because then whitespace is ignored and `#` is a special character too.

##### Returns

`string`

#### Remarks

Such enclosed substring in a regular expression is interpreted as a literal string. This function also escapes `\E`, so that it does not end the literal string.