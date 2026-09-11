# Operator `Au.Types.DpiOf.implicit operator`

## Overload 1

```csharp
public static implicit operator DpiOf(int dpi)
```

##### Parameters

- *dpi*  (`int`)

##### Returns

`Au.Types.DpiOf`

* * *

## Overload 2

```csharp
public static implicit operator DpiOf(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Returns

`Au.Types.DpiOf`

##### Exceptions

- `Au.Types.AuWndException`:
  Invalid window handle.

* * *

## Overload 3

```csharp
public static implicit operator DpiOf(Control c)
```

##### Parameters

- *c*  (`Control`)

##### Returns

`Au.Types.DpiOf`

##### Exceptions

- `ArgumentNullException`
- `Au.Types.AuWndException`:
  Invalid window handle.

* * *

## Overload 4

```csharp
public static implicit operator DpiOf(DependencyObject c)
```

##### Parameters

- *c*  (`DependencyObject`)

##### Returns

`Au.Types.DpiOf`

##### Exceptions

- `ArgumentNullException`
- `Au.Types.AuWndException`:
  Invalid window handle.

* * *

## Overload 5

```csharp
public static implicit operator DpiOf(nint hMonitor)
```

##### Parameters

- *hMonitor*  (`nint`)

##### Returns

`Au.Types.DpiOf`

* * *

## Overload 6

```csharp
public static implicit operator DpiOf(POINT screenOf)
```

##### Parameters

- *screenOf*  (`Au.Types.POINT`)

##### Returns

`Au.Types.DpiOf`

* * *

## Overload 7

```csharp
public static implicit operator DpiOf(RECT screenOf)
```

##### Parameters

- *screenOf*  (`Au.Types.RECT`)

##### Returns

`Au.Types.DpiOf`

* * *

## Overload 8

```csharp
public static implicit operator int(DpiOf d)
```

##### Parameters

- *d*  (`Au.Types.DpiOf`)

##### Returns

`int`