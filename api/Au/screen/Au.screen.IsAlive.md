# Property `Au.screen.IsAlive`

True if the screen handle is valid.

```
public bool IsAlive { get; }
```

##### Property Value

`bool`

#### Remarks

Don't use with variables that hold a callback function. This function does not call it and returns `false`.