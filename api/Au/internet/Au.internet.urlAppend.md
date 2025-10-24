# Method `Au.internet.urlAppend`

Joins a URL address and parameters. Urlencodes parameters.

```
public static string urlAppend(string address, params string[] parameters)
```

##### Parameters

- *address*  (`string`):
    URL part without parameters or with some parameters. The function does not modify it.
- *parameters*  (`string[]`):
    URL parameters to append, like `"name1=value1", "name2=value2"`. The function urlencodes them (`System.Net.WebUtility.UrlEncode`).

##### Returns

`string`

String like `"address?name1=value1&name2=value2"`.

##### Exceptions

- `ArgumentException`:
    Incorrect format of a parameters string.