# Method `Au.Types.AuException.ThrowIfHresultNegative`

If *errorCode* is less than 0, throws `Au.Types.AuException` that includes the code and its message. More info: `Au.Types.AuException.FormatMessage`.

```
public static void ThrowIfHresultNegative(int errorCode, string message = null)
```

##### Parameters

- *errorCode*  (`int`):
    Windows API error code or `HRESULT`.
- *message*  (`string`):
    Main message. The message of the error code will be appended to it.