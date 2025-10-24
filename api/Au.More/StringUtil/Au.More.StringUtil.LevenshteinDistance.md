# Method `Au.More.StringUtil.LevenshteinDistance`

Calculates the Levenshtein distance between two strings, which tells how much they are different.

```
public static int LevenshteinDistance(ReadOnlySpan<char> s1, ReadOnlySpan<char> s2)
```

##### Parameters

- *s1*  (`ReadOnlySpan<char>`)
- *s2*  (`ReadOnlySpan<char>`)

##### Returns

`int`

#### Remarks

It is the number of character edits (removals, inserts, replacements) that must occur to get from string *s1* to string *s2*. Can be used to measure similarity and match approximate strings with fuzzy logic. Uses code and info from https://www.dotnetperls.com/levenshtein.