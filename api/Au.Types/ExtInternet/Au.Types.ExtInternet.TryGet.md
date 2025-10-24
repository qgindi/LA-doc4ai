# Method `Au.Types.ExtInternet.TryGet`

Sends a GET request to the specified URL, and gets the response. Handles HTTP errors and exceptions.

```
public static bool TryGet(this HttpClient t, out HttpResponseMessage r, string url, bool dontWait = false, IEnumerable<string> headers = null, bool printError = false, string auth = null, Action<HttpRequestMessage> also = null)
```

##### Parameters

- *t*  (`HttpClient`)
- *r*  (`HttpResponseMessage`):
    Receives `HttpResponseMessage` object that can be used to get response content (web page HTML, JSON, file, etc), headers etc. See example. Will be `null` if failed because of an exception.
- *url*  (`string`):
    URL. To create URL with urlencoded parameters you can use `Au.internet.urlAppend`.
- *dontWait*  (`bool`):
    Use `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`.
- *headers*  (`IEnumerable<string>`):
    `null` or request headers like `["name1: value1", "name2: value2"]`. Also you can add headers to `System.Net.Http.HttpClient.DefaultRequestHeaders`, like `internet.http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");`.
- *printError*  (`bool`):
    If failed, call `Au.print.warning`.
- *auth*  (`string`):
    String like `"username:password"` for basic authentication. It will be encoded and sent in the `Authorization` header. For other authentication schemes use the *headers* parameter instead, like `headers: ["Authorization: Bearer token"]`.
- *also*  (`Action<HttpRequestMessage>`):
    Can set more properties for the request.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `UriFormatException`:
    Invalid URL format.
- `Exception`:
    If *headers* used, exceptions of `Au.Types.ExtInternet.AddMany`.

#### Examples

```
if (!internet.http.TryGet(out var r, "https://httpbin.org/anything", printError: true)) return;
print.it(r.Text());
```