# Method `Au.internet.jsonContent`

Creates `System.Net.Http.HttpContent` for posting JSON. It can be used with functions like `System.Net.Http.HttpClient.PostAsync` and `Au.Types.ExtInternet.Post`.

```
public static HttpContent jsonContent(object x, JsonSerializerOptions options = null)
```

##### Parameters

- *x*  (`object`):
    JSON string, or `System.Text.Json.Nodes.JsonNode` (or a derived type), or object of any type that can be serialized to JSON with `System.Text.Json.JsonSerializer`.
- *options*  (`JsonSerializerOptions`)

##### Returns

`HttpContent`

If *x* is string, creates/returns new `System.Net.Http.StringContent`. Else if *x* is `System.Text.Json.Nodes.JsonNode` (or a derived type), calls `System.Text.Json.Nodes.JsonNode.ToJsonString` and creates/returns new `System.Net.Http.StringContent`. Else if *x* is `System.Net.Http.HttpContent` (or a derived type), returns *x*. Else calls/returns `System.Net.Http.Json.JsonContent.Create`.

##### Exceptions

- `Exception`:
    Exceptions of `System.Net.Http.Json.JsonContent.Create`.

#### Examples

```
var v = new { a = "A", b = true };
string s = internet.http.Post("https://httpbin.org/anything", internet.jsonContent(v)).Text();
```