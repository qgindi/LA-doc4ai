# Property `Au.Types.JSettings.SerializerOptions`

Default deserialization and serialization options.

```csharp
public static JsonSerializerOptions SerializerOptions { get; }
```

##### Property Value

`JsonSerializerOptions`

```csharp
	AllowTrailingCommas = true,
	DefaultIgnoreCondition = JsonIgnoreCondition.WhenWritingNull,
	Encoder = JavaScriptEncoder.UnsafeRelaxedJsonEscaping,
	IncludeFields = true,
	IgnoreReadOnlyFields = true,
	IgnoreReadOnlyProperties = true,
	WriteIndented = true,
```