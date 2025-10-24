# Property `Au.Types.HSContentPart.Name`

Gets name from `Content-Disposition` header.

```
public string Name { get; }
```

##### Property Value

`string`

If `Content-Disposition` header or name is missing, returns `Index.ToS()`.

#### Remarks

Decodes `"=?utf-8?B?base64?="`.