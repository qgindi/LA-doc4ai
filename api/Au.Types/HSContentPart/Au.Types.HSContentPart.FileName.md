# Property `Au.Types.HSContentPart.FileName`

Gets filename from `Content-Disposition` header.

```
public string FileName { get; }
```

##### Property Value

`string`

`null` if `Content-Disposition` header or filename is missing.

#### Remarks

Decodes `"utf-8''urlencoded"` or `"=?utf-8?B?base64?="`.