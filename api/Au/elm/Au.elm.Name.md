# Property `Au.elm.Name`

Gets name.

```
public string Name { get; }
```

##### Property Value

`string`

`""` if name is unavailable or if failed. Supports `Au.lastError`.

#### Remarks

UI element name usually is its read-only text (eg button text, link text), or its adjacent read-only text (eg text label by this edit box). It usually does not change, therefore can be used to find or identify the UI element.