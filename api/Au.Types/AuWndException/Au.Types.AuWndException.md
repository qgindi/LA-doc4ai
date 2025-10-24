# Class `Au.Types.AuWndException`

Exception thrown mostly by `Au.wnd` functions.

```
public class AuWndException : AuException, ISerializable
```

##### Remarks

Some constructors support Windows API error code. Then `Au.Types.AuWndException.Message` also will contain its error description. If error code `ERROR_INVALID_WINDOW_HANDLE`, `Au.Types.AuWndException.Message` also depends on whether the window handle is 0. If parameter *errorCode* is 0 or not used: if the window handle is invalid, uses `ERROR_INVALID_WINDOW_HANDLE`. If the string passed to the constructor starts with `"*"`, replaces the `"*"` with `"Failed to "`. If ends with `"*"`, replaces the `"*"` with `" window."`. If does not end with `"."`, appends `"."`.

##### Inheritance

`object` → `Exception` → `Au.Types.AuException` → `AuWndException`

### Constructors

`AuWndException(wnd, int, string, Exception)`, `AuWndException(wnd, string, Exception)`

### Properties

`Message`, `Window`

### Members inherited from other types of this library
`AuException.NativeErrorCode`, `AuException.FormattedMessage`, `AuException.FormatMessage()`, `AuException.ThrowIfHresultNot0()`, `AuException.ThrowIfHresultNegative()`