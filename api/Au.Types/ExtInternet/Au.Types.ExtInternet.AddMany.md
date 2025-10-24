# Method `Au.Types.ExtInternet.AddMany`

## Overload 1

Adds multiple HTTP request headers. Uses `System.Net.Http.Headers.HttpHeaders.Add`.

```
public static void AddMany(this HttpRequestHeaders t, params string[] headers)
```

##### Parameters

- *t*  (`HttpRequestHeaders`)
- *headers*  (`string[]`):
    Headers like `"name1: value1", "name2: value2"`.

##### Exceptions

- `ArgumentException`:
    Incorrect format of a *headers* string.
- `Exception`:
    Exceptions of `System.Net.Http.Headers.HttpHeaders.Add`.

* * *

## Overload 2

Adds multiple HTTP request headers. Uses `System.Net.Http.Headers.HttpHeaders.Add`.

```
public static void AddMany(this HttpRequestHeaders t, IEnumerable<string> headers)
```

##### Parameters

- *t*  (`HttpRequestHeaders`)
- *headers*  (`IEnumerable<string>`):
    Headers like `"name1: value1", "name2: value2"`.

##### Exceptions

- `ArgumentException`:
    Incorrect format of a *headers* string.
- `Exception`:
    Exceptions of `System.Net.Http.Headers.HttpHeaders.Add`.