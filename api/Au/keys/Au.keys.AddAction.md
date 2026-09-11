# Method `Au.keys.AddAction`

Adds a callback function.

```csharp
public keys AddAction(Action a)
```

##### Parameters

- *a*  (`Action`)

##### Returns

`Au.keys`

This.

#### Remarks

The callback function will be called by `Au.keys.SendNow` and can do anything except sending keys and copy/paste.