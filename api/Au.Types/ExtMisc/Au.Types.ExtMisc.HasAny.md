# Method `Au.Types.ExtMisc.HasAny`

Returns `true` if this enum variable has one or more flag bits specified in *flags*.

```
public static bool HasAny<T>(this T t, T flags) where T : unmanaged, Enum
```

##### Parameters

- *t*  (`T`)
- *flags*  (`T`):
    One or more flags.

##### Returns

`bool`

##### Type Parameters

- `T`