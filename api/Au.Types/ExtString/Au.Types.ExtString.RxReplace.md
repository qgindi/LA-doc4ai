# Method `Au.Types.ExtString.RxReplace`

## Overload 1

Finds and replaces all match instances of PCRE regular expression *rx*.

```
public static string RxReplace(this string t, string rx, string repl, int maxCount = -1, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *repl*  (`string`):
    Replacement pattern. Can consist of any combination of literal text and substitutions like `$1`. Supports .NET regular expression substitution syntax. See `System.Text.RegularExpressions.Regex.Replace`. Also: replaces `$*` with the name of the last encountered mark; replaces `${+func}` etc with the return value of a function registered with `Au.regexp.addReplaceFunc`.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid regular expression.
    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.

* * *

## Overload 2

Finds and replaces all match instances of PCRE regular expression *rx*.

```
public static int RxReplace(this string t, string rx, string repl, out string result, int maxCount = -1, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *repl*  (`string`):
    Replacement pattern. Can consist of any combination of literal text and substitutions like `$1`. Supports .NET regular expression substitution syntax. See `System.Text.RegularExpressions.Regex.Replace`. Also: replaces `$*` with the name of the last encountered mark; replaces `${+func}` etc with the return value of a function registered with `Au.regexp.addReplaceFunc`.
- *result*  (`string`):
    The result string. Can be the same variable as the subject string.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`int`

The number of replacements made. Returns the result string through an out parameter.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid regular expression.
    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.

* * *

## Overload 3

Finds and replaces all match instances of PCRE regular expression *rx*. Uses a callback function.

```
public static string RxReplace(this string t, string rx, Func<RXMatch, string> replFunc, int maxCount = -1, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *replFunc*  (`Func<Au.Types.RXMatch, string>`):
    Callback function's delegate, eg lambda. Called for each found match. Returns the replacement. In the callback function you can use `Au.Types.RXMatch.ExpandReplacement`.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid regular expression.
    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.

* * *

## Overload 4

Finds and replaces all match instances of PCRE regular expression *rx*. Uses a callback function.

```
public static int RxReplace(this string t, string rx, Func<RXMatch, string> replFunc, out string result, int maxCount = -1, RXFlags flags = 0, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *replFunc*  (`Func<Au.Types.RXMatch, string>`):
    Callback function's delegate, eg lambda. Called for each found match. Returns the replacement. In the callback function you can use `Au.Types.RXMatch.ExpandReplacement`.
- *result*  (`string`):
    The result string. Can be the same variable as the subject string.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.

##### Returns

`int`

The number of replacements made. Returns the result string through an out parameter.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid regular expression.
    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    Failed (unlikely).
- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

More info and examples: `Au.regexp`.