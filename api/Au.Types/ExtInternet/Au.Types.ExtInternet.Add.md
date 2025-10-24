# Method `Au.Types.ExtInternet.Add`

Adds a non-file field. Uses `System.Net.Http.MultipartFormDataContent.Add`.

```
public static MultipartFormDataContent Add(this MultipartFormDataContent t, string name, string value)
```

##### Parameters

- *t*  (`MultipartFormDataContent`)
- *name*  (`string`)
- *value*  (`string`)

##### Returns

`MultipartFormDataContent`

This.

##### Exceptions

- `ArgumentException`:
    See `System.Net.Http.MultipartFormDataContent.Add`.