# Method `Au.Types.JSettings.Dispose`

## Overload 1

Saves now if need, and releases used resources. In the future will not save or reload.
Don't need to call if the settings are used until process exit.

```csharp
public void Dispose()
```

##### Implements

`IDisposable.Dispose()`

* * *

## Overload 2

```csharp
protected virtual void Dispose(bool disposing)
```

##### Parameters

- *disposing*  (`bool`)