# Property `Au.Types.HSContentType.Encoding`

Gets text encoding.

```
public Encoding Encoding { get; }
```

##### Property Value

`Encoding`

Returns:

- `null` if multipart content (`Au.Types.HSContentType.Boundary` not `null`).
- UTF-8 if `charset` is `utf-8` or not specified.
- `Encoding` that matches `charset`.
- ASCII if `charset` is invalid.