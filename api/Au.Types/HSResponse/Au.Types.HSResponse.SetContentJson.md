# Method `Au.Types.HSResponse.SetContentJson`

## Overload 1

JSON-serializes object of type `T`, and sets `Au.Types.HSResponse.Content`. Also sets `Content-Type` header.

```
public void SetContentJson<T>(T obj, string contentType = "application/json; charset=utf-8")
```

##### Parameters

- *obj*  (`T`):
    Object of type `T`.
- *contentType*  (`string`):
    If not `null`, sets `Content-Type` header.

##### Exceptions

- `Exception`:
    Exceptions of `System.Text.Json.JsonSerializer.SerializeToUtf8Bytes<TValue>`.

##### Type Parameters

- `T`

* * *

## Overload 2

JSON-serializes object of specified type, and sets `Au.Types.HSResponse.Content`. Also sets `Content-Type` header.

```
public void SetContentJson<T>(object obj, Type type, string contentType = "application/json; charset=utf-8")
```

##### Parameters

- *obj*  (`object`):
    Object.
- *type*  (`Type`):
    *obj* type.
- *contentType*  (`string`):
    If not `null`, sets `Content-Type` header.

##### Exceptions

- `Exception`:
    Exceptions of `System.Text.Json.JsonSerializer.SerializeToUtf8Bytes<TValue>`.

##### Type Parameters

- `T`