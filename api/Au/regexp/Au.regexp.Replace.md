# Method `Au.regexp.Replace`

## Overload 1

Finds and replaces all match instances of the regular expression.

```
public string Replace(string s, string repl = null, int maxCount = -1, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *repl*  (`string`):
    Replacement pattern. Can consist of any combination of literal text and substitutions like `$1`. Supports .NET regular expression substitution syntax. See `System.Text.RegularExpressions.Regex.Replace`. Also: replaces `$*` with the name of the last encountered mark; replaces `${+func}` etc with the return value of a function registered with `Au.regexp.addReplaceFunc`.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Replace`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
s = x.Replace(s, "'$2$1'");
print.it(s);
```

* * *

## Overload 2

Finds and replaces all match instances of the regular expression.

```
public int Replace(string s, string repl, out string result, int maxCount = -1, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *repl*  (`string`):
    Replacement pattern. Can consist of any combination of literal text and substitutions like `$1`. Supports .NET regular expression substitution syntax. See `System.Text.RegularExpressions.Regex.Replace`. Also: replaces `$*` with the name of the last encountered mark; replaces `${+func}` etc with the return value of a function registered with `Au.regexp.addReplaceFunc`.
- *result*  (`string`):
    The result string. Can be the same variable as the subject string.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`int`

The number of replacements made. Returns the result string through an out parameter.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Replace`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(0 == x.Replace(s, "'$2$1'", out s)) print.it("not found");
else print.it(s);
```

* * *

## Overload 3

Finds and replaces all match instances of the regular expression. Uses a callback function.

```
public string Replace(string s, Func<RXMatch, string> replFunc, int maxCount = -1, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *replFunc*  (`Func<Au.Types.RXMatch, string>`):
    Callback function's delegate, eg lambda. Called for each found match. Returns the replacement. In the callback function you can use `Au.Types.RXMatch.ExpandReplacement`.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Replace`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
s = x.Replace(s, o => o.Value.Upper());
print.it(s);
```

* * *

## Overload 4

Finds and replaces all match instances of the regular expression. Uses a callback function.

```
public int Replace(string s, Func<RXMatch, string> replFunc, out string result, int maxCount = -1, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *replFunc*  (`Func<Au.Types.RXMatch, string>`):
    Callback function's delegate, eg lambda. Called for each found match. Returns the replacement. In the callback function you can use `Au.Types.RXMatch.ExpandReplacement`.
- *result*  (`string`):
    The result string. Can be the same variable as the subject string.
- *maxCount*  (`int`):
    Maximal count of replacements to make. If -1 (default), replaces all.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`int`

The number of replacements made. Returns the result string through an out parameter.

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:

    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.
- `Au.Types.AuException`:
    The PCRE API function `pcre2_match` failed. Unlikely.

#### Remarks

This function is similar to `System.Text.RegularExpressions.Regex.Replace`.

#### Examples

```
var s = "one two22 three333 four";
var x = new regexp(@"\b(\w+?)(\d+)\b");
if(0 == x.Replace(s, o => o.Value.Upper(), out s)) print.it("not found");
else print.it(s);
```