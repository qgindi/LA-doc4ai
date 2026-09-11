# Constructor of `Au.regexp`

Compiles regular expression string.

```csharp
public regexp(string rx, RXFlags flags = 0)
```

##### Parameters

- *rx*  (`string`):
  Regular expression. Cannot be `null`.
- *flags*  (`Au.Types.RXFlags`):
  Options.
  Default 0. Flag UTF is implicitly added if*rx* contains non-ASCII characters and not used flag `NEVER_UTF`.

##### Exceptions

- `ArgumentNullException`
- `ArgumentException`:
  Invalid regular expression. Or failed to compile it for some other reason (unlikely).

#### Remarks

Calls PCRE API function [pcre2_compile](🔗).

PCRE regular expression syntax: [full](🔗), [short](🔗).

Examples in class help: `Au.regexp`.