# Method `Au.internet.message`

Creates `System.Net.Http.HttpRequestMessage` for `System.Net.Http.HttpClient.Send` or `System.Net.Http.HttpClient.SendAsync` in the same way as the `System.Net.Http.HttpClient` extension methods of this library (**ExtInternet.Get**, **ExtInternet.Post** etc).

```
public static HttpRequestMessage message(HttpMethod method, string url, IEnumerable<string> headers = null, HttpContent content = null, string auth = null)
```

##### Parameters

- *method*  (`HttpMethod`):
    `System.Net.Http.HttpMethod.Post` etc.
- *url*  (`string`):
    URL. To create URL with urlencoded parameters you can use `Au.internet.urlAppend`.
- *headers*  (`IEnumerable<string>`):
    `null` or request headers like `["name1: value1", "name2: value2"]`. Also you can add headers to `System.Net.Http.HttpClient.DefaultRequestHeaders`, like `internet.http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");`.
- *content*  (`HttpContent`)
- *auth*  (`string`):
    String like `"username:password"` for basic authentication. It will be encoded and sent in the `Authorization` header. For other authentication schemes use the *headers* parameter instead, like `headers: ["Authorization: Bearer token"]`.

##### Returns

`HttpRequestMessage`

#### Examples

```
using System.Net.Http;
var m = internet.message(HttpMethod.Get, "https://www.example.com");
var r = internet.http.Send(m);
print.it(r.Text());
```