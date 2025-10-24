# Method `Au.Types.ExtString.RxMatch`

## Overload 1

Returns `true` if this string matches PCRE regular expression *rx*. Gets match info as `Au.Types.RXMatch`.

```
public static bool RxMatch(this string t, string rx, out RXMatch result, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string. If `null`, returns `false`.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *result*  (`Au.Types.RXMatch`):
    Receives match info.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the match and all groups that exist in the regular expressions.
- If partial match, returns `true`, and *result* contains the match without groups. Partial match is possible if used a `PARTIAL_` flag.
- If no match, returns `false`, and *result* normally is `null`. But if a mark is available, *result* is an object with two valid properties - `Au.Types.RXMatch.Exists` (`false`) and `Au.Types.RXMatch.Mark`; other properties have undefined values or throw exception.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid regular expression.
- `Au.Types.AuException`:
    Failed (unlikely).

#### Remarks

More info and examples: `Au.regexp`.

* * *

## Overload 2

Returns `true` if this string matches PCRE regular expression *rx*. Gets whole match or some group, as string.

```
public static bool RxMatch(this string t, string rx, int group, out string result, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string. If `null`, returns `false`.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *group*  (`int`):
    Group number (1-based index) of result. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`string`):
    Receives the match value.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the value of the match or of the specifed group.
- If partial match, returns `true`. Partial match is possible if used a `PARTIAL_` flag. Then cannot get groups, therefore *group* should be 0.
- If no match, returns `false`, and *result* is `null`.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `ArgumentException`:
    Invalid regular expression.
- `Au.Types.AuException`:
    Failed (unlikely).

#### Remarks

More info and examples: `Au.regexp`.

* * *

## Overload 3

Returns `true` if this string matches PCRE regular expression *rx*. Gets whole match or some group, as index and length.

```
public static bool RxMatch(this string t, string rx, int group, out RXGroup result, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string. If `null`, returns `false`.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *group*  (`int`):
    Group number (1-based index) of result. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`Au.Types.RXGroup`):
    Receives match info.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the match or the specified group.
- If partial match, returns `true`. Partial match is possible if used a `PARTIAL_` flag. Then cannot get groups, therefore *group* should be 0.
- If no match, returns `false`, and *result* is empty.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `ArgumentException`:
    Invalid regular expression.
- `Au.Types.AuException`:
    Failed (unlikely).

#### Remarks

More info and examples: `Au.regexp`.