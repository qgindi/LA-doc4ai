# Method `Au.pathname.isUrl`

Returns `true` if the string starts with a URL protocol name (existing or not) and `':'` character. Calls `Au.pathname.getUrlProtocolLength` and returns `true` if it's not 0.

```
public static bool isUrl(ReadOnlySpan<char> s)
```

##### Parameters

- *s*  (`ReadOnlySpan<char>`):
    A URL or path or any string. Can be `null`.

##### Returns

`bool`

#### Remarks

URL examples: `"http:"`, `"http://www.x.com"`, `"file:///path"`, `"shell:etc"`.