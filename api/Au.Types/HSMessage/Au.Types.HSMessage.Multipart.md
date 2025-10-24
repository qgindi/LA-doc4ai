# Property `Au.Types.HSMessage.Multipart`

Parts of multipart content. For example of POST content with `Content-Type: multipart/form-data`.

```
public Dictionary<string, HSContentPart> Multipart { get; }
```

##### Property Value

`Dictionary<string, Au.Types.HSContentPart>`

`null` if the message has no multipart content.