# Constructor of `Au.Types.DpiOf`

## Overload 1

```csharp
public DpiOf(int dpi)
```

##### Parameters

- *dpi*  (`int`)

* * *

## Overload 2

```csharp
public DpiOf(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Exceptions

- `Au.Types.AuWndException`:
  Invalid window handle.

* * *

## Overload 3

```csharp
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

```csharp
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

```csharp
public DpiOf(nint hMonitor)
```

##### Parameters

- *hMonitor*  (`nint`)

* * *

## Overload 6

```csharp
public DpiOf(POINT screenOf)
```

##### Parameters

- *screenOf*  (`Au.Types.POINT`)

* * *

## Overload 7

```csharp
public DpiOf(RECT screenOf)
```

##### Parameters

- *screenOf*  (`Au.Types.RECT`)