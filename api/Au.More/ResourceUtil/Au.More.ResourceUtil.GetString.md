# Method `Au.More.ResourceUtil.GetString`

Gets string.

```
public static string GetString(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"myString"` or `"file.txt"` or `"sub/file.txt"`. More info: `Au.More.ResourceUtil`.

##### Returns

`string`

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    Unsupported resource type.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.

#### Remarks

Supports resources of type `string`, `byte[]` (UTF-8), stream (UTF-8).