# Method `Au.computer.lockOrSwitchUser`

Initiates computer lock operation.

```csharp
public static bool lockOrSwitchUser()
```

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

Uses API `LockWorkStation`.