# Method `Au.Types.ExtInternet.Post`

Sends a POST request to the specified URL, and gets the response.

```
public static HttpResponseMessage Post(this HttpClient t, string url, HttpContent content, IEnumerable<string> headers = null, bool dontWait = false, string auth = null, Action<HttpRequestMessage> also = null)
```

##### Parameters

- *t*  (`HttpClient`)
- *url*  (`string`):
    URL.
- *content*  (`HttpContent`):
    Data to post. Usually web form data (see `Au.internet.formContent`) or JSON (see `Au.internet.jsonContent`). Can be `null`.
- *headers*  (`IEnumerable<string>`):
    `null` or request headers like `["name1: value1", "name2: value2"]`. Also you can add headers to `System.Net.Http.HttpClient.DefaultRequestHeaders`, like `internet.http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");`.
- *dontWait*  (`bool`):
    Use `System.Net.Http.HttpCompletionOption.ResponseHeadersRead`.
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

#### Examples

Post form data. Note: the `using` will close the file stream. Don't need it when content does not contain files.

```
using var content = internet.formContent(("name1", "value1"), ("name2", "value2")).AddFile("name3", @"C:\Test\file.png");
string s = internet.http.Post("https://httpbin.org/anything", content).Text();
```

Post object as JSON.

```
var v = new { a = "A", b = true };
string s = internet.http.Post("https://httpbin.org/anything", internet.jsonContent(v)).Text();
print.it(s);
```