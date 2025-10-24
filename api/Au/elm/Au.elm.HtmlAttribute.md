# Method `Au.elm.HtmlAttribute`

Gets a HTML attribute.

```
public string HtmlAttribute(string name)
```

##### Parameters

- *name*  (`string`):
    Attribute name, for example `"href"`, `"id"`, `"class"`. Full, case-sensitive.

##### Returns

`string`

`""` if this is not a HTML element or does not have the specified attribute or failed. Supports `Au.lastError`.

##### Exceptions

- `ArgumentException`:
    *name* is `null`/`""`/invalid.

#### Remarks

Works with Chrome, Internet Explorer and apps that use their code (Edge, Opera, web browser controls...). This UI element must be found without flag `NotInProc`.