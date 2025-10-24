# Property `Au.uacInfo.Failed`

Returns `true` if the last called property function failed. Normally it should never fail. Only `Au.uacInfo.ofProcess` can fail (then it returns `null`).

```
public bool Failed { get; }
```

##### Property Value

`bool`