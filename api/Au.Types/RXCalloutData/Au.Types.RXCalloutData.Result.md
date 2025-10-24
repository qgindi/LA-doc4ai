# Property `Au.Types.RXCalloutData.Result`

Sets the return value of the callout function, as documented in PCRE help topic [pcre2callout](https://www.pcre.org/current/doc/html/pcre2callout.html).

```
public int Result { set; }
```

##### Property Value

`int`

#### Remarks

Default 0. If 1, matching fails at the current point, but the testing of other matching possibilities goes ahead, just as if a lookahead assertion had failed. If -1 (`PCRE2_ERROR_NOMATCH`), the match function returns `false` (no match). Values less tan -2 are PCRE error codes and cause exception.