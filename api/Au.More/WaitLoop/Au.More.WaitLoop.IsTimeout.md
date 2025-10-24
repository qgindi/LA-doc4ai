# Method `Au.More.WaitLoop.IsTimeout`

If the timeout time is not expired, returns `false`. Else if the timeout was negative, returns `true`. Else throws `System.TimeoutException`.

```
public bool IsTimeout()
```

##### Returns

`bool`

##### Exceptions

- `TimeoutException`