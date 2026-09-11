# Property `Au.internet.http`

Gets a static `System.Net.Http.HttpClient` instance that can be used in scripts to download web pages, files, post web form data, etc.

```csharp
public static HttpClient http { get; }
```

##### Property Value

`HttpClient`

#### Remarks

Creates `System.Net.Http.HttpClient` only the first time; later just returns it.

Sets these properties and default headers:

- `System.Net.Http.SocketsHttpHandler.AutomaticDecompression` = `All`.
- `User-Agent: Au`.

Does not change the default timeout (100 s). To download large files without a timeout, use `Au.Types.ExtInternet.Download` (or `DownloadAsync`). See example in Cookbook.

`internet.http` makes easier to discover and use internet get/post/etc functions when using this library. You can instead create an `System.Net.Http.HttpClient` instance and use its functions in the same way. See the second example. Use the same `HttpClient` instance when making multiple get/post/etc requests.

#### Examples

```csharp
string s = internet.http.Get("https://httpbin.org/anything").Text();
```

Without `internet.http`.

```csharp
using var http = new HttpClient();
http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");
string s = http.Get("https://httpbin.org/anything").Text();
```

Or.

```csharp
using var http = new HttpClient() { BaseAddress = new("https://httpbin.org") };
http.DefaultRequestHeaders.Add("User-Agent", "Script/1.0");
string s = http.Get("anything").Text();
```