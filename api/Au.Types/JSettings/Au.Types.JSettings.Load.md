# Method `Au.Types.JSettings.Load`

Loads a JSON file and deserializes to an object of type `T`, or creates a new object of type `T`.

```
protected static T Load<T>(string file, bool useDefault = false, bool? useDefaultOnError = true, JsonSerializerOptions jsOpt = null) where T : JSettings
```

##### Parameters

- *file*  (`string`):
    Full path of `.json` file. If `null`, does not load and will not save.
- *useDefault*  (`bool`):
    Use default settings. Don't load from *file*. Delete *file* if exists.
- *useDefaultOnError*  (`bool?`):
    What to do if failed to load or parse the file: `true` (default) - backup (rename) the file and use default settings; `false` - throw exception (for example `System.Text.Json.JsonException` if invalid JSON); `null` - show dialog with options to exit or use default settings.
- *jsOpt*  (`JsonSerializerOptions`):
    Options for deserializing and serializing. If `null`, uses `Au.Types.JSettings.SerializerOptions`.

##### Returns

`T`

Object of type `T`. Either deserialized from file or new object with default values.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `NotSupportedException`:
    Field type not supported by `System.Text.Json.JsonSerializer`.

##### Type Parameters

- `T`