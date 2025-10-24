# Method `Au.Types.ExtString.RxFindAll`

## Overload 1

Finds all match instances of PCRE regular expression *rx*.

```
public static IEnumerable<RXMatch> RxFindAll(this string t, string rx, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`IEnumerable<Au.Types.RXMatch>`

A lazy `IEnumerable<RXMatch>` that can be used with `foreach`.

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

* * *

## Overload 2

Finds all match instances of PCRE regular expression *rx*. Gets array of `Au.Types.RXMatch`.

```
public static bool RxFindAll(this string t, string rx, out RXMatch[] result, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *result*  (`Au.Types.RXMatch[]`):
    Receives all found matches.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`bool`

`true` if found 1 or more matches.

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

* * *

## Overload 3

Finds all match instances of PCRE regular expression *rx*.

```
public static IEnumerable<string> RxFindAll(this string t, string rx, int group, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *group*  (`int`):
    Group number (1-based index) of results. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`IEnumerable<string>`

A lazy `IEnumerable<string>` that can be used with `foreach`.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `ArgumentException`:
    Invalid regular expression. Or used a `PARTIAL_` flag.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.

* * *

## Overload 4

Finds all match instances of PCRE regular expression *rx*. Gets array of strings.

```
public static bool RxFindAll(this string t, string rx, int group, out string[] result, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *group*  (`int`):
    Group number (1-based index) of results. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`string[]`):
    Receives all found matches.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`bool`

`true` if found 1 or more matches.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `ArgumentException`:
    Invalid regular expression. Or used a `PARTIAL_` flag.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.