# Method `Au.Types.HSResponse.SetContentText`

Sets response content text.

```
public void SetContentText(string content, string contentType = "text/plain; charset=utf-8")
```

##### Parameters

- *content*  (`string`):
    Sets `Au.Types.HSResponse.Content`: `Content = content.ToUTF8();`.
- *contentType*  (`string`):
    If not `null`, sets `Content-Type` header.