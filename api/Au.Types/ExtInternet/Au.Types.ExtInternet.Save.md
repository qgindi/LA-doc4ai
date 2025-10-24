# Method `Au.Types.ExtInternet.Save`

Saves content in a file. Downloads if need.

```
public static HttpResponseMessage Save(this HttpResponseMessage t, string file)
```

##### Parameters

- *t*  (`HttpResponseMessage`)
- *file*  (`string`):
    File path. The function uses `Au.pathname.normalize`. Creates parent directory if need.

##### Returns

`HttpResponseMessage`

This.

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request.
- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.Net.Http.HttpContent.ReadAsStream`, `System.IO.File.Create` and other used functions.

#### Remarks

By default `System.Net.Http.HttpClient` downloads content to a memory buffer before returning. To avoid it, use *completionOption* `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`, or `Au.Types.ExtInternet.Get` with *dontWait* `true`. Then call this function (it will download the file), and finally dispose the `System.Net.Http.HttpResponseMessage`.

### See Also

`Au.Types.ExtInternet.Get`