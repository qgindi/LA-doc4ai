# Method `Au.Types.ExtInternet.DownloadAsync`

## Overload 1

The async version of `Au.Types.ExtInternet.Download`.

```
public static Task<bool> DownloadAsync(this HttpResponseMessage t, Stream stream, Action<ProgressArgs> progress = null, CancellationToken cancel = default, bool disposeStream = false, string progressText1 = null)
```

##### Parameters

- *t*  (`HttpResponseMessage`)
- *stream*  (`Stream`):
    Writes to this stream.
- *progress*  (`Action<Au.Types.ProgressArgs>`):
    Calls this callback function to report the progress. If `null`, shows standard progress dialog.
- *cancel*  (`CancellationToken`):
    Can be used to cancel.
- *disposeStream*  (`bool`):
    Call `stream.Dispose();`.
- *progressText1*  (`string`):
    Progress dialog heading text. Default: `"Downloading"`.

##### Returns

`Task<bool>`

`false` if canceled.

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request.
- `Exception`:
    Other exceptions.

#### Remarks

By default `System.Net.Http.HttpClient` downloads content to a memory buffer before returning. To avoid it, use *completionOption* `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`, or `Au.Types.ExtInternet.Get` with *dontWait* `true`. Then call this function (it will download the file), and finally dispose the `System.Net.Http.HttpResponseMessage`.

Cannot provide the progress percentage if the content length is unknown. Top reasons:

- The HTTP server uses chunked transfer encoding.
- The HTTP server uses content compression and the `System.Net.Http.HttpClient` is configured to automatically decompress (for example `Au.internet.http`). Instead of `internet.http` create a `System.Net.Http.HttpClient` and optionally set header `"Accept-Encoding: br, gzip, deflate"`. This function will decompress.

* * *

## Overload 2

The async version of `Au.Types.ExtInternet.Download`.

```
public static Task<bool> DownloadAsync(this HttpResponseMessage t, string file, Action<ProgressArgs> progress = null, CancellationToken cancel = default)
```

##### Parameters

- *t*  (`HttpResponseMessage`)
- *file*  (`string`):
    File path. The function uses `Au.pathname.normalize`. Creates parent directory if need.
- *progress*  (`Action<Au.Types.ProgressArgs>`):
    Calls this callback function to report the progress. If `null`, shows standard progress dialog.
- *cancel*  (`CancellationToken`):
    Can be used to cancel.

##### Returns

`Task<bool>`

`false` if canceled.

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request.
- `Exception`:
    Other exceptions.

#### Remarks

By default `System.Net.Http.HttpClient` downloads content to a memory buffer before returning. To avoid it, use *completionOption* `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`, or `Au.Types.ExtInternet.Get` with *dontWait* `true`. Then call this function (it will download the file), and finally dispose the `System.Net.Http.HttpResponseMessage`.

Cannot provide the progress percentage if the content length is unknown. Top reasons:

- The HTTP server uses chunked transfer encoding.
- The HTTP server uses content compression and the `System.Net.Http.HttpClient` is configured to automatically decompress (for example `Au.internet.http`). Instead of `internet.http` create a `System.Net.Http.HttpClient` and optionally set header `"Accept-Encoding: br, gzip, deflate"`. This function will decompress.

#### Examples

```
if (!internet.http.Get(url, true).Download(zip)) return;
```