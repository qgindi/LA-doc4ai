# Constructor of `Au.Types.AuWndException`

## Overload 1

Sets `Au.Types.AuWndException.Message` = *message* (default `"Failed."`). Sets `Au.Types.AuException.NativeErrorCode` = `w.IsAlive ? 0 : ERROR_INVALID_WINDOW_HANDLE`.

```
public AuWndException(wnd w, string message = "Failed.", Exception innerException = null)
```

##### Parameters

- *w*  (`Au.wnd`)
- *message*  (`string`)
- *innerException*  (`Exception`)

* * *

## Overload 2

Sets `Au.Types.AuException.NativeErrorCode` = `(errorCode != 0) ? errorCode : (w.IsAlive ? lastError.code : ERROR_INVALID_WINDOW_HANDLE)`. Sets `Au.Types.AuWndException.Message` = `message + " " + lastError.messageFor(NativeErrorCode)`.

```
public AuWndException(wnd w, int errorCode, string message = "Failed.", Exception innerException = null)
```

##### Parameters

- *w*  (`Au.wnd`)
- *errorCode*  (`int`)
- *message*  (`string`)
- *innerException*  (`Exception`)