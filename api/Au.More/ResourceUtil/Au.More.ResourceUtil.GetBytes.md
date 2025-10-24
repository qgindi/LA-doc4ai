# Method `Au.More.ResourceUtil.GetBytes`

Gets `byte[]`.

```
public static byte[] GetBytes(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"file.txt"` or `"sub/file.txt"`. More info: `Au.More.ResourceUtil`.

##### Returns

`byte[]`

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    Unsupported resource type.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.

#### Remarks

Supports resources of type `byte[]`, `string` (gets UTF-8 bytes), stream.