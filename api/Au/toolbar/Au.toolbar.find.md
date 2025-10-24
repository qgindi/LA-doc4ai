# Method `Au.toolbar.find`

Finds an open toolbar by `Au.toolbar.Name`.

```
public static toolbar find(string name)
```

##### Parameters

- *name*  (`string`)

##### Returns

`Au.toolbar`

`null` if not found or closed or never shown (`Au.toolbar.Show` not called).

#### Remarks

Finds only toolbars created in the same script and thread.

Does not find satellite toolbars. Use this code: `toolbar.find("owner toolbar").Satellite`