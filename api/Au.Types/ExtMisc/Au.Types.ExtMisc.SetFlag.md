# Method `Au.Types.ExtMisc.SetFlag`

Adds or removes a flag or flags.

```
public static void SetFlag<T>(this ref T t, T flag, bool add) where T : unmanaged, Enum
```

##### Parameters

- *t*  (`T`)
- *flag*  (`T`):
    One or more flags to add or remove.
- *add*  (`bool`):
    If `true`, adds flag, else removes flag.

##### Type Parameters

- `T`