# Method `Au.Types.ExtString.RxIsMatch`

Returns `true` if this string matches PCRE regular expression *rx*.

```
public static bool RxIsMatch(this string t, string rx, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string. If `null`, returns `false`.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`bool`

`true` if full or partial match. Partial match is possible if used a `PARTIAL_` flag.

##### Exceptions

- `ArgumentException`:
    Invalid regular expression.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `Au.Types.AuException`:
    Failed (unlikely).

#### Remarks

More info and examples: `Au.regexp`.