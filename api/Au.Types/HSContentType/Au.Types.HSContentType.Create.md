# Method `Au.Types.HSContentType.Create`

Creates from `Content-Type` header.

```
public static HSContentType Create(Dictionary<string, string> headers)
```

##### Parameters

- *headers*  (`Dictionary<string, string>`)

##### Returns

`Au.Types.HSContentType`

`null` if `Content-Type` header is missing or invalid.