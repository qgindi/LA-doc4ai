# Method `Au.More.ResourceUtil.Get`

Gets resource of any type.

```
public static T Get<T>(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"file.txt"` or `"sub/file.txt"`. More info: `Au.More.ResourceUtil`.

##### Returns

`T`

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    The resource is of different type. This function does not convert.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.

##### Type Parameters

- `T`