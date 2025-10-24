# Property `Au.inputBlocker.Pause`

Gets or sets whether the blocking is paused.

```
public bool Pause { get; set; }
```

##### Property Value

`bool`

#### Remarks

The `set` function is much faster than `Au.inputBlocker.Stop`/`Au.inputBlocker.Start`. Does not remove hooks etc. Discards blocked keys.