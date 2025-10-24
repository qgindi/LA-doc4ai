# Constructor of `Au.screen`

## Overload 1

Creates variable with screen handle, aka `HMONITOR`.

```
public screen(nint handle)
```

##### Parameters

- *handle*  (`nint`)

* * *

## Overload 2

Creates "lazy" variable that calls your function to get screen when need.

```
public screen(Func<screen> f)
```

##### Parameters

- *f*  (`Func<Au.screen>`)