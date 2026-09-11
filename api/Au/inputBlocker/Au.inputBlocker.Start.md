# Method `Au.inputBlocker.Start`

Starts blocking.

```csharp
public void Start(BIEvents what)
```

##### Parameters

- *what*  (`Au.Types.BIEvents`):
  Enum: None, Keys, MouseClicks, MouseMoving, All.

##### Exceptions

- `ArgumentException`:
  *what* is 0.
- `InvalidOperationException`:
  Already started.