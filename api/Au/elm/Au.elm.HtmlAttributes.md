# Method `Au.elm.HtmlAttributes`

Gets all HTML attributes.

```
public Dictionary<string, string> HtmlAttributes()
```

##### Returns

`Dictionary<string, string>`

Empty dictionary if this is not a HTML element or does not have attributes or failed. Supports `Au.lastError`.

#### Remarks

Works with Chrome, Internet Explorer and apps that use their code (Edge, Opera, web browser controls...). This UI element must be found without flag `NotInProc`.