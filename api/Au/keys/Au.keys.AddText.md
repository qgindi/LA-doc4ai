# Method `Au.keys.AddText`

## Overload 1

Adds text or HTML. It will be sent by `Au.keys.SendNow`.

```
public keys AddText(string text, string html = null)
```

##### Parameters

- *text*  (`string`):
    Text. Can be `null`.
- *html*  (`string`):
    HTML. Can be full HTML or fragment. See `Au.clipboardData.AddHtml`. Can be specified only *text* or only *html* or both. If both, will paste *html* in apps that support it, elsewhere *text*. If only *html*, in apps that don't support HTML will paste *html* as text.

##### Returns

`Au.keys`

This.

#### Remarks

To send text can use keys, characters or clipboard, depending on `Au.opt.key` and text. If *html* not `null`, uses clipboard.

* * *

## Overload 2

Adds text with explicitly specified sending method (keys, characters or paste).

```
public keys AddText(string text, OKeyText how)
```

##### Parameters

- *text*  (`string`):
    Text. Can be `null`.
- *how*  (`Au.Types.OKeyText`):
    Overrides `Au.Types.OKey.TextHow`.

##### Returns

`Au.keys`

This.