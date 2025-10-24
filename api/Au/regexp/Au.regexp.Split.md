# Method `Au.regexp.Split`

Returns an array of substrings that in the subject string are delimited by regular expression matches.

```
public string[] Split(string s, int maxCount = 0, Range? range = null, RXMatchFlags matchFlags = 0)
```

##### Parameters

- *s*  (`string`):
    Subject string. Cannot be `null`.
- *maxCount*  (`int`):
    Maximal count of substrings to get. The last substring contains the unsplit remainder of the subject string. If 0 (default) or negative, gets all.
- *range*  (`Range?`):
    Start and end offsets in the subject string. If `null` (default), uses whole string. Examples: `i..j` (from `i` to `j`), `i..` (from `i `to the end), `..j` (from 0 to `j`). The subject part before the start index is not ignored if regular expression starts with a lookbehind assertion or anchor, eg `^` or `\b` or `(?<=...)`. Instead of `^` you can use `\G` or flag `RXFlags.ANCHORED`. More info in PCRE documentation topic [pcre2api](https://www.pcre.org/current/doc/html/pcre2api.html), chapter "The string to be matched by pcre2_match()". The subject part after the end index is always ignored.
- *matchFlags*  (`Au.Types.RXMatchFlags`):
    Options. The same options also can be set in `Au.regexp` constructor's *flags*. Constructor's flags and *matchFlags* are added, which means that *matchFlags* cannot unset flags set by constructor.

##### Returns

`string[]`

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

Element 0 of the returned array is *s* substring until the first match of the regular expression, element 1 is substring between the first and second match, and so on. If no matches, the array contains single element and it is *s*.

This function is similar to `System.Text.RegularExpressions.Regex.Split`.

#### Examples

```
var s = "one, two,three , four";
var x = new regexp(@" *, *");
var a = x.Split(s);
for(int i = 0; i < a.Length; i++) print.it(i, a[i]);
```