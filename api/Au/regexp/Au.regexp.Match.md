# Method `Au.regexp.Match`

## Overload 1

Returns `true` if string *s* matches this regular expression. Gets match info as `Au.Types.RXMatch`.

```
public bool Match(string s, out RXMatch result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *result*  (`Au.Types.RXMatch`):
    Receives match info.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the match and all groups that exist in the regular expressions.
- If partial match, returns `true`, and *result* contains the match without groups. Partial match is possible if used a `PARTIAL_` flag.
- If no match, returns `false`, and *result* normally is `null`. But if a mark is available, *result* is an object with two valid properties - `Au.Types.RXMatch.Exists` (`false`) and `Au.Types.RXMatch.Mark`; other properties have undefined values or throw exception.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Match`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(x.Match(s, out var m)) print.it(m.Value, m[1].Value, m[2].Value);
```

* * *

## Overload 2

Returns `true` if string *s* matches this regular expression. Gets whole match or some group, as `Au.Types.RXGroup` (index, length, value).

```
public bool Match(string s, int group, out RXGroup result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *group*  (`int`):
    Group number (1-based index) of result. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`Au.Types.RXGroup`):
    Receives match info.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the match or the specified group.
- If partial match, returns `true`. Partial match is possible if used a `PARTIAL_` flag. Then cannot get groups, therefore *group* should be 0.
- If no match, returns `false`, and *result* is empty.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is a simplified version of `Au.regexp.Match(string, out RXMatch, Range?, RXMatchFlags)`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(x.Match(s, 0, out RXGroup g)) print.it(g.Value, g.Start);
```

* * *

## Overload 3

Returns `true` if string *s* matches this regular expression. Gets whole match or some group, as string.

```
public bool Match(string s, int group, out string result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *group*  (`int`):
    Group number (1-based index) of result. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`string`):
    Receives the match value.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the value of the match or of the specifed group.
- If partial match, returns `true`. Partial match is possible if used a `PARTIAL_` flag. Then cannot get groups, therefore *group* should be 0.
- If no match, returns `false`, and *result* is `null`.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is a simplified version of `Au.regexp.Match(string, out RXMatch, Range?, RXMatchFlags)`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(x.Match(s, 0, out string v)) print.it(v);
```

* * *

## Overload 4

Returns `true` if string span *s* matches this regular expression. Gets whole match or some group, as `Au.Types.StartEnd`.

```
public bool Match(ReadOnlySpan<char> s, int group, out StartEnd result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`ReadOnlySpan<char>`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *group*  (`int`):
    Group number (1-based index) of result. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`Au.Types.StartEnd`):
    Receives match info.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

- If full match, returns `true`, and *result* contains the match or the specified group.
- If partial match, returns `true`. Partial match is possible if used a `PARTIAL_` flag. Then cannot get groups, therefore *group* should be 0.
- If no match, returns `false`, and *result* is empty.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is a simplified version of `Au.regexp.Match(string, out RXMatch, Range?, RXMatchFlags)`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(x.Match(s, 0, out RXGroup g)) print.it(g.Value, g.Start);
```

* * *

## Overload 5

Returns `true` if string span *s* matches this regular expression. Writes match info to caller-allocated memory (array, stackalloc array, etc).

```
public bool Match(ReadOnlySpan<char> s, Span<StartEnd> result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`ReadOnlySpan<char>`):
    Subject string. If `null`, returns `false`, even if the regular expression matches empty string.
- *result*  (`Span<Au.Types.StartEnd>`):
    Receives match info: main match in `result[0]` and group matches in other elements. `result.Length` must be equal to the number of groups + 1. If a group does not exists, the element's `start` and `end` are `-1`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.
- `ArgumentException`:
    *result* array too short.