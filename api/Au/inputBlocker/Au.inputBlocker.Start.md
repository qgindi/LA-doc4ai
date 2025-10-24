# Method `Au.inputBlocker.Start`

Starts blocking.

```
public void Start(BIEvents what)
```

##### Parameters

- *what*  (`Au.Types.BIEvents`)

##### Exceptions

- `ArgumentException`:
    *what* is 0.
- `InvalidOperationException`:
    Already started.