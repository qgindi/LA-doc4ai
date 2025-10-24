# Constructor of `Au.Types.AuException`

## Overload 1

Sets `Au.Types.AuException.Message` = *message* (default `"Failed."`). Sets `Au.Types.AuException.NativeErrorCode` = 0.

```
public AuException(string message = "Failed.", Exception innerException = null)
```

##### Parameters

- *message*  (`string`)
- *innerException*  (`Exception`)

* * *

## Overload 2

Sets `Au.Types.AuException.NativeErrorCode` = `(errorCode != 0) ? errorCode : lastError.code`. Sets `Au.Types.AuException.Message` = `message + " " + lastError.messageFor(NativeErrorCode)`.

```
public AuException(int errorCode, string message = "Failed.", Exception innerException = null)
```

##### Parameters

- *errorCode*  (`int`)
- *message*  (`string`)
- *innerException*  (`Exception`)