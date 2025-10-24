# Property `Au.toolbar.Satellite`

A toolbar attached to this toolbar. Can be `null`.

```
public toolbar Satellite { get; set; }
```

##### Exceptions

- `InvalidOperationException`:
    The `set` function throws this exception if the satellite toolbar was attached to another toolbar or was shown as non-satellite toolbar.

##### Property Value

`Au.toolbar`

#### Remarks

The satellite toolbar is shown when mouse enters its owner toolbar and hidden when mouse leaves it and its owner. Like an "auto hide" feature. A toolbar can have multiple satellite toolbars at different times. A satellite toolbar can be attached/detached multiple times to the same toolbar.