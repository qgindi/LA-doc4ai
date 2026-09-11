# Constructor of `Au.inputBlocker`

## Overload 1

This constructor does nothing (does not call `Au.inputBlocker.Start`).

```csharp
public inputBlocker()
```

* * *

## Overload 2

This constructor calls `Au.inputBlocker.Start`.

```csharp
public inputBlocker(BIEvents what)
```

##### Parameters

- *what*  (`Au.Types.BIEvents`):
  Enum: None, Keys, MouseClicks, MouseMoving, All.

##### Exceptions

- `ArgumentException`:
  *what* is 0.