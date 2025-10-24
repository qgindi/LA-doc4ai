# Method `Au.wildex.Match`

Compares a string with the [wildcard expression](../articles/Wildcard%20expression.html) used to create this `Au.wildex`. Returns `true` if they match.

```
public bool Match(string s)
```

##### Parameters

- *s*  (`string`):
    String. If `null`, returns `false`. If `""`, returns `true` if it was `""` or `"*"` or a regular expression that matches `""`.

##### Returns

`bool`