# Method `Au.Types.WProp.GetList`

Gets list of window properties.
Uses API`EnumPropsEx`.

```csharp
public Dictionary<string, nint> GetList()
```

##### Returns

`Dictionary<string, nint>`

0-length list if failed. Fails if invalid window or access denied ([UAC](🔗)). Supports `Au.lastError`.