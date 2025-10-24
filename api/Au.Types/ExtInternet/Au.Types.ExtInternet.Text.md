# Method `Au.Types.ExtInternet.Text`

Gets content text as string. Downloads it if need.

```
public static string Text(this HttpResponseMessage t, bool ignoreError = false)
```

##### Parameters

- *t*  (`HttpResponseMessage`)
- *ignoreError*  (`bool`):
    Don't call `System.Net.Http.HttpResponseMessage.EnsureSuccessStatusCode`.

##### Returns

`string`

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request. No exception if *ignoreError* `true`.
- `Exception`:
    Exceptions of `System.Net.Http.HttpContent.ReadAsStringAsync`.