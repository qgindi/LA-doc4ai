# Method `Au.Types.ExtString.RxSplit`

Returns an array of substrings that in this string are delimited by regular expression matches.

```
public static string[] RxSplit(this string t, string rx, int maxCount = 0, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *maxCount*  (`int`):
    Maximal count of substrings to get. The last substring contains the unsplit remainder of the subject string. If 0 (default) or negative, gets all.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`string[]`

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid regular expression. Or used a `PARTIAL_` flag.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.