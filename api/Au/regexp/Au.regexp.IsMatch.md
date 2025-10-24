# Method `Au.regexp.IsMatch`

## Overload 1

Returns `true` if string *s* matches this regular expression.

```
public bool IsMatch(string s, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

`true` if full or partial match. Partial match is possible if used a `PARTIAL_` flag.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.IsMatch`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
print.it(x.IsMatch(s));
```

* * *

## Overload 2

Returns `true` if string *s* matches this regular expression.

```
public bool IsMatch(ReadOnlySpan<char> s, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`ReadOnlySpan<char>`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

`true` if full or partial match. Partial match is possible if used a `PARTIAL_` flag.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.IsMatch`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
print.it(x.IsMatch(s));
```