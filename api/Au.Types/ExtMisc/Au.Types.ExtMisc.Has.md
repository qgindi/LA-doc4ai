# Method `Au.Types.ExtMisc.Has`

Returns `true` if this enum variable has all flag bits specified in *flag*.

```
public static bool Has<T>(this T t, T flag) where T : unmanaged, Enum
```

##### Parameters

- *t*  (`T`)
- *flag*  (`T`):
    One or more flags.

##### Returns

`bool`

##### Type Parameters

- `T`

#### Remarks

The same as code `(t & flag) == flag` or `System.Enum.HasFlag`.