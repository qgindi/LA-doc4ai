# Method `Au.Types.HSMessage.Json`

## Overload 1

JSON-deserializes `Au.Types.HSMessage.Content` to object of type `T`.

```
public T Json<T>()
```

##### Returns

`T`

`default(T)` if the request does not have body data.

##### Exceptions

- `Exception`:
    Exceptions of `System.Text.Json.JsonSerializer.Deserialize<TValue>`.

##### Type Parameters

- `T`

* * *

## Overload 2

JSON-deserializes `Au.Types.HSMessage.Content` to object of specified type.

```
public object Json(Type type)
```

##### Parameters

- *type*  (`Type`)

##### Returns

`object`

`null` if the request does not have body data.

##### Exceptions

- `Exception`:
    Exceptions of `System.Text.Json.JsonSerializer.Deserialize`.