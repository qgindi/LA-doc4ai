# Method `Au.Types.ExtInternet.Json`

## Overload 1

Parses content, which must be JSON, and returns the root node. Then you can access JSON elements like `var y = (string)r["x"]["y"];`. Downloads content if need. Uses `System.Text.Json.Nodes.JsonNode.Parse`.

```
public static JsonNode Json(this HttpResponseMessage t, bool ignoreError = false)
```

##### Parameters

- *t*  (`HttpResponseMessage`)
- *ignoreError*  (`bool`):
    Don't call `System.Net.Http.HttpResponseMessage.EnsureSuccessStatusCode`.

##### Returns

`JsonNode`

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request. No exception if *ignoreError* `true`.
- `Exception`:
    Exceptions of `System.Net.Http.HttpContent.ReadAsByteArrayAsync`.
- `JsonException`:
    Failed to parse JSON.

* * *

## Overload 2

Parses content, which must be JSON. From it creates/returns an object of type *T*. Downloads content if need. Uses `System.Net.Http.Json.HttpContentJsonExtensions.ReadFromJsonAsync<T>`.

```
public static T Json<T>(this HttpResponseMessage t)
```

##### Parameters

- *t*  (`HttpResponseMessage`)

##### Returns

`T`

##### Exceptions

- `HttpRequestException`:
    Failed HTTP request.
- `Exception`:
    Exceptions of `ReadFromJsonAsync`.

##### Type Parameters

- `T`