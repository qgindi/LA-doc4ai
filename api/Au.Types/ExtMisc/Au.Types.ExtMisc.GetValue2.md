# Method `Au.Types.ExtMisc.GetValue2`

Gets a value from a subkey of this registry key.

```
public static object GetValue2(this RegistryKey t, string subkey, string name, object defaultValue = null, RegistryValueOptions options = RegistryValueOptions.None)
```

##### Parameters

- *t*  (`RegistryKey`)
- *subkey*  (`string`):
    The name or relative path of the subkey.
- *name*  (`string`):
    The name of the value to retrieve.
- *defaultValue*  (`object`):
    The value to return if *subkey* or *name* does not exist.
- *options*  (`RegistryValueOptions`)

##### Returns

`object`

The value associated with *name*, or *defaultValue* if *subkey* or *name* not found.

##### Exceptions

- `Exception`:
    Exceptions of `Microsoft.Win32.RegistryKey.OpenSubKey` and `Microsoft.Win32.RegistryKey.GetValue`.

#### Remarks

Calls `Microsoft.Win32.RegistryKey.OpenSubKey` and `Microsoft.Win32.RegistryKey.GetValue`.