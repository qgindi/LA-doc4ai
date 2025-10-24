# Method `Au.Types.RXMatch.ExpandReplacement`

Returns expanded version of the specified replacement pattern.

```
public string ExpandReplacement(string repl)
```

##### Parameters

- *repl*  (`string`):
    Replacement pattern. Can consist of any combination of literal text and substitutions like `$1`. Supports .NET regular expression substitution syntax. See `System.Text.RegularExpressions.Regex.Replace`. Also: replaces `$*` with the name of the last encountered mark; replaces `${+func}` and `${+func(n)}` with the return value of a function registered with `Au.regexp.addReplaceFunc`.

##### Returns

`string`

##### Exceptions

- `ArgumentException`:

    - Invalid `$replacement`.
    - Used a `PARTIAL_` flag.
    - The regular expression contains `(?=...\K)`.

#### Remarks

Works like `System.Text.RegularExpressions.Match.Result`. See also: `Au.regexp.Replace`.