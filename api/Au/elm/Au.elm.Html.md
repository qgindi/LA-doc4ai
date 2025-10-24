# Method `Au.elm.Html`

Gets HTML.

```
public string Html(bool outer)
```

##### Parameters

- *outer*  (`bool`):
    If `true`, gets outer HTML (with tag and attributes), else inner HTML.

##### Returns

`string`

`""` if this is not a HTML element or if failed. Supports `Au.lastError`.

#### Remarks

Works with Chrome, Internet Explorer and apps that use their code (Edge, Opera, web browser controls...). This UI element must be found without flag `NotInProc`. If this is the root of web page (role `DOCUMENT` or `PANE`), gets web page body HTML.