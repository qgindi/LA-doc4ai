# Method `Au.Types.ExtInternet.Get`

## Overload 1

Sends a GET request to the specified URL, and gets the response.

```
public static HttpResponseMessage Get(this HttpClient t, string url, bool dontWait = false, IEnumerable<string> headers = null, string auth = null, Action<HttpRequestMessage> also = null)
```

##### Parameters

- *t*  (`HttpClient`)
- *url*  (`string`):
    URL. To create URL with urlencoded parameters you can use `Au.internet.urlAppend`.
- *dontWait*  (`bool`):
    Use `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`.
- *headers*  (`IEnumerable<string>`):
    `null` or request headers like `["name1: value1", "name2: value2"]`. Also you can add headers to `System.Net.Http.HttpClient.DefaultRequestHeaders`, like `internet.http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");`.
- *auth*  (`string`):
    String like `"username:password"` for basic authentication. It will be encoded and sent in the `Authorization` header. For other authentication schemes use the *headers* parameter instead, like `headers: ["Authorization: Bearer token"]`.
- *also*  (`Action<HttpRequestMessage>`):
    Can set more properties for the request.

##### Returns

`HttpResponseMessage`

An `HttpResponseMessage` object that can be used to get response content (web page HTML, JSON, file, etc), headers etc. To get content use `Au.Types.ExtInternet.Text` etc.

##### Exceptions

- `Exception`:
    Exceptions of `System.Net.Http.HttpClient.Send`. If *headers* used, exceptions of `Au.Types.ExtInternet.AddMany`.
- `UriFormatException`:
    Invalid URL format.

#### Examples

```
string s = internet.http.Get("https://httpbin.org/anything").Text();
```

* * *

## Overload 2

Sends a GET request to the specified URL, and gets the response. Saves the response content (file, web page, etc) in a file.

```
public static HttpResponseMessage Get(this HttpClient t, string url, string resultFile, IEnumerable<string> headers = null, string auth = null, Action<HttpRequestMessage> also = null)
```

##### Parameters

- *t*  (`HttpClient`)
- *url*  (`string`):
    URL. To create URL with urlencoded parameters you can use `Au.internet.urlAppend`.
- *resultFile*  (`string`):
    File path. The function uses `Au.pathname.normalize`. Creates parent directory if need.
- *headers*  (`IEnumerable<string>`):
    `null` or request headers like `["name1: value1", "name2: value2"]`. Also you can add headers to `System.Net.Http.HttpClient.DefaultRequestHeaders`, like `internet.http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");`.
- *auth*  (`string`):
    String like `"username:password"` for basic authentication. It will be encoded and sent in the `Authorization` header. For other authentication schemes use the *headers* parameter instead, like `headers: ["Authorization: Bearer token"]`.
- *also*  (`Action<HttpRequestMessage>`):
    Can set more properties for the request.

##### Returns

`HttpResponseMessage`

An `HttpResponseMessage` object that contains response headers etc. Rarely used.

##### Exceptions

- `Exception`:
    Exceptions of `System.Net.Http.HttpClient.Send` and `Au.Types.ExtInternet.Save`. If *headers* used, exceptions of `Au.Types.ExtInternet.AddMany`.