# Method `Au.Types.WFCache.Clear`

Clears all cached properties, or only name.

```
public void Clear(bool onlyName = false)
```

##### Parameters

- *onlyName*  (`bool`):
    Clear only name (because it may change, unlike other cached properties).

#### Remarks

Usually don't need to call this function. It is implicitly called when the variable is used with a new window.