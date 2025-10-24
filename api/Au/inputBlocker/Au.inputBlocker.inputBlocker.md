# Constructor of `Au.inputBlocker`

## Overload 1

This constructor does nothing (does not call `Au.inputBlocker.Start`).

```
public inputBlocker()
```

* * *

## Overload 2

This constructor calls `Au.inputBlocker.Start`.

```
public inputBlocker(BIEvents what)
```

##### Parameters

- *what*  (`Au.Types.BIEvents`)

##### Exceptions

- `ArgumentException`:
    *what* is 0.