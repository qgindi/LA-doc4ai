# Method `Au.Types.ExtInternet.Bytes`

Gets content data as `byte[]`. Downloads it if need. If content is text, the array contains that text, usually UTF-8.

```
public static byte[] Bytes(this HttpResponseMessage t, bool ignoreError = false)
```

##### Parameters

- *t*  (`HttpResponseMessage`)
- *ignoreError*  (`bool`):
    Don't call `System.Net.Http.HttpResponseMessage.EnsureSuccessStatusCode`.

##### Returns

`byte[]`

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request. No exception if *ignoreError* `true`.
- `Exception`:
    Exceptions of `System.Net.Http.HttpContent.ReadAsByteArrayAsync`.