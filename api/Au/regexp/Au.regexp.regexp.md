# Constructor of `Au.regexp`

Compiles regular expression string.

```
public regexp(string rx, RXFlags flags = 0)
```

##### Parameters

- *rx*  (`string`):
    Regular expression. Cannot be `null`.
- *flags*  (`Au.Types.RXFlags`):
    Options. Default 0. Flag UTF is implicitly added if *rx* contains non-ASCII characters and not used flag `NEVER_UTF`.

##### Exceptions

- `ArgumentNullException`
- `ArgumentException`:
    Invalid regular expression. Or failed to compile it for some other reason (unlikely).

#### Remarks

Calls PCRE API function [pcre2_compile](https://www.pcre.org/current/doc/html/pcre2api.html).

PCRE regular expression syntax: [full](https://www.pcre.org/current/doc/html/pcre2pattern.html), [short](https://www.pcre.org/current/doc/html/pcre2syntax.html).

Examples in class help: `Au.regexp`.