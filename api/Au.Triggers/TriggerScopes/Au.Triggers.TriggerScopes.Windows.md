# Method `Au.Triggers.TriggerScopes.Windows`

Sets scope "only these windows". Hotkey, autotext and mouse triggers added afterwards will work only when one of the specified windows is active.

```
public TriggerScope Windows(params wndFinder[] any)
```

##### Parameters

- *any*  (`Au.wndFinder[]`):
    Specifies windows, like `new("Window1"), new("Window2")`.

##### Returns

`Au.Triggers.TriggerScope`

Returns an object that can be later passed to `Au.Triggers.TriggerScopes.Again` to reuse this scope.