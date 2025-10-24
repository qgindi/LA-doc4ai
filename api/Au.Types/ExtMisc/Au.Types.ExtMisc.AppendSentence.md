# Method `Au.Types.ExtMisc.AppendSentence`

Appends string as new correctly formatted sentence.

```
public static StringBuilder AppendSentence(this StringBuilder t, string s, bool noUcase = false)
```

##### Parameters

- *t*  (`StringBuilder`)
- *s*  (`string`)
- *noUcase*  (`bool`):
    Don't make the first character uppercase.

##### Returns

`StringBuilder`

this.

#### Remarks

If *s* is `null` or `""`, does nothing. If this is not empty, appends space. If *s* starts with a lowercase character, makes it uppercase, unless this ends with a character other than `'.'`. Appends `'.'` if *s* does not end with `'.'`, `';'`, `':'`, `','`, `'!'` or `'?'`.