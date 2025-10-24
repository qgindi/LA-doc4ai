# Method `Au.pathname.getUrlProtocolLength`

Gets the length of the URL protocol name (also known as URI scheme) in string, including `':'`. If the string does not start with a protocol name, returns 0.

```
public static int getUrlProtocolLength(ReadOnlySpan<char> s)
```

##### Parameters

- *s*  (`ReadOnlySpan<char>`):
    A URL or path or any string. Can be `null`.

##### Returns

`int`

#### Remarks

URL examples: `"http:"` (returns 5), `"http://www.x.com"` (returns 5), `"file:///path"` (returns 5), `"shell:etc"` (returns 6).

The protocol can be unknown. The function just checks string format, which is an ASCII alpha character followed by one or more ASCII alpha-numeric, `'.'`, `'-'`, `'+'` characters, followed by `':'` character.