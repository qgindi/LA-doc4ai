# Class `Au.Types.InputDesktopException`

This exception is thrown when current thread is not on the input desktop and therefore cannot use mouse, keyboard, clipboard and window functions. For example when PC locked (`Win+L`), screen saver, UAC consent, `Ctrl+Alt+Delete` or not in the active user session.

```
public class InputDesktopException : AuException, ISerializable
```

##### Inheritance

`object` → `Exception` → `Au.Types.AuException` → `InputDesktopException`

### Constructors

`InputDesktopException(string)`

### Methods

`ThrowIfBadDesktop`

### See Also

`Au.miscInfo.isInputDesktop`

### Members inherited from other types of this library
`AuException.NativeErrorCode`, `AuException.Message`, `AuException.FormattedMessage`, `AuException.FormatMessage()`, `AuException.ThrowIfHresultNot0()`, `AuException.ThrowIfHresultNegative()`