# Property `Au.elm.DefaultAction`

Gets default action of `Au.elm.Invoke`.

```
public string DefaultAction { get; }
```

##### Property Value

`string`

`""` if this property is unavailable or if failed. Supports `Au.lastError`.

#### Remarks

If this is a Java UI element, returns all actions that can be used with `Au.elm.JavaInvoke`, like `"action1, action2, action3"`, from which the first is considered default and is used by `Au.elm.Invoke`. Note: the string is supposed to be localized, ie depends on UI language; except Java.