# Operator `Au.Types.WContains.implicit operator`

## Overload 1

```
public static implicit operator WContains(wndChildFinder f)
```

##### Parameters

- *f*  (`Au.wndChildFinder`)

##### Returns

`Au.Types.WContains`

* * *

## Overload 2

```
public static implicit operator WContains(elmFinder f)
```

##### Parameters

- *f*  (`Au.elmFinder`)

##### Returns

`Au.Types.WContains`

* * *

## Overload 3

```
public static implicit operator WContains(uiimageFinder f)
```

##### Parameters

- *f*  (`Au.uiimageFinder`)

##### Returns

`Au.Types.WContains`

* * *

## Overload 4

```
public static implicit operator WContains(ocrFinder f)
```

##### Parameters

- *f*  (`Au.ocrFinder`)

##### Returns

`Au.Types.WContains`

* * *

## Overload 5

Converts from string to `Au.wndChildFinder`, `Au.elmFinder`, `Au.uiimageFinder` or `Au.ocrFinder`. See `Au.wnd.find`.

```
public static implicit operator WContains(string s)
```

##### Parameters

- *s*  (`string`)

##### Returns

`Au.Types.WContains`

##### Exceptions

- `Exception`:
    Exceptions of constructor of `Au.wndChildFinder`, `Au.elmFinder`, `Au.uiimageFinder` or `Au.ocrFinder`.