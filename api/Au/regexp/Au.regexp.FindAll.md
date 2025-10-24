# Method `Au.regexp.FindAll`

## Overload 1

Finds all match instances of the regular expression.

```
public IEnumerable<RXMatch> FindAll(string s, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`IEnumerable<Au.Types.RXMatch>`

A lazy `IEnumerable<RXMatch>` that can be used with `foreach`.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Matches`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
foreach(var m in x.FindAll(s)) print.it(m.Value, m[1].Value, m[2].Value);
```

* * *

## Overload 2

Finds all match instances of the regular expression.

```
public IEnumerable<string> FindAll(string s, int group, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *group*  (`int`):
    Group number (1-based index) of results. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`IEnumerable<string>`

A lazy `IEnumerable<string>` that can be used with `foreach`.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `ArgumentException`:

    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Matches`.

#### Examples

```
var s = "one two three";
var x = new regexp(@"\b\w+\b");
foreach(var v in x.FindAll(s, 0)) print.it(v);
```

* * *

## Overload 3

Finds all match instances of the regular expression. Gets array of `Au.Types.RXMatch`.

```
public bool FindAll(string s, out RXMatch[] result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *result*  (`Au.Types.RXMatch[]`):
    Receives all found matches.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

`true` if found 1 or more matches.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Matches`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(!x.FindAll(s, out var a)) { print.it("not found"); return; }
foreach(var m in a) print.it(m.Value, m[1].Value, m[2].Value);
```

* * *

## Overload 4

Finds all match instances of the regular expression. Gets array of strings.

```
public bool FindAll(string s, int group, out string[] result, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *group*  (`int`):
    Group number (1-based index) of results. If 0 - whole match. See also `Au.regexp.GetGroupNumberOf`.
- *result*  (`string[]`):
    Receives all found matches.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`bool`

`true` if found 1 or more matches.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *group* or *range*.
- `ArgumentException`:

    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Matches`.

#### Examples

```
var s = "one two three";
var x = new regexp(@"\b\w+\b");
if(!x.FindAll(s, 0, out var a)) { print.it("not found"); return; }
foreach(var v in a) print.it(v);
```