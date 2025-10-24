# Class `Au.Types.AuException`

The base exception class used in this library. Thrown when something fails and there is no better exception type for that failure.

```
public class AuException : Exception, ISerializable
```

##### Remarks

Some constructors support Windows API error code. Then `Au.Types.AuException.Message` will contain its error description. If the string passed to the constructor starts with `"*"`, replaces the `"*"` with `"Failed to "`. If does not end with `"."`, appends `"."`.

##### Inheritance

`object` → `Exception` → `AuException`

Derived: `Au.Types.AuWndException`, `Au.Types.InputDesktopException`

### Constructors

`AuException(int, string, Exception)`, `AuException(string, Exception)`

### Fields

`FormattedMessage`

### Properties

`Message`, `NativeErrorCode`

### Methods

`FormatMessage`, `ThrowIfHresultNegative`, `ThrowIfHresultNot0`