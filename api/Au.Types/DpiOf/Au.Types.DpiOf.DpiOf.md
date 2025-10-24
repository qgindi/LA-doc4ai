# Constructor of `Au.Types.DpiOf`

## Overload 1

```
public DpiOf(int dpi)
```

##### Parameters

- *dpi*  (`int`)

* * *

## Overload 2

```
public DpiOf(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window handle.

* * *

## Overload 3

```
public DpiOf(Control c)
```

##### Parameters

- *c*  (`Control`)

##### Exceptions

- `ArgumentNullException`
- `Au.Types.AuWndException`:
    Invalid window handle.

* * *

## Overload 4

```
public DpiOf(DependencyObject c)
```

##### Parameters

- *c*  (`DependencyObject`)

##### Exceptions

- `ArgumentNullException`
- `Au.Types.AuWndException`:
    Invalid window handle.

* * *

## Overload 5

```
public DpiOf(nint hMonitor)
```

##### Parameters

- *hMonitor*  (`nint`)

* * *

## Overload 6

```
public DpiOf(POINT screenOf)
```

##### Parameters

- *screenOf*  (`Au.Types.POINT`)

* * *

## Overload 7

```
public DpiOf(RECT screenOf)
```

##### Parameters

- *screenOf*  (`Au.Types.RECT`)