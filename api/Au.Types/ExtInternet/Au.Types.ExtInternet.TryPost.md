# Method `Au.Types.ExtInternet.TryPost`

Sends a POST request to the specified URL, and gets the response. Handles HTTP errors and exceptions.

```
public static bool TryPost(this HttpClient t, out HttpResponseMessage r, string url, HttpContent content, IEnumerable<string> headers = null, bool printError = false, bool dontWait = false, string auth = null, Action<HttpRequestMessage> also = null)
```

##### Parameters

- *t*  (`HttpClient`)
- *r*  (`HttpResponseMessage`):
    Receives `HttpResponseMessage` object that can be used to get response content (web page HTML, JSON, file, etc), headers etc. See example. Will be `null` if failed because of an exception.
- *url*  (`string`):
    URL.
- *content*  (`HttpContent`):
    Data to post. Usually web form data (see `Au.internet.formContent`) or JSON (see `Au.internet.jsonContent`). Can be `null`.
- *headers*  (`IEnumerable<string>`):
    `null` or request headers like `["name1: value1", "name2: value2"]`. Also you can add headers to `System.Net.Http.HttpClient.DefaultRequestHeaders`, like `internet.http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");`.
- *printError*  (`bool`):
    If failed, call `Au.print.warning`.
- *dontWait*  (`bool`):
    Use `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`.
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

Post form data.

```
var content = internet.formContent(("name1", "value1"), ("name2", "value2"));
if (!internet.http.TryPost(out var r, "https://httpbin.org/anything", content, printError: true)) return;
print.it(r.Text());
```

Post object as JSON.

```
var v = new { a = "A", b = true };
if (!internet.http.TryPost(out var r, "https://httpbin.org/anything", internet.jsonContent(v), printError: true)) return;
print.it(r.Text());
```