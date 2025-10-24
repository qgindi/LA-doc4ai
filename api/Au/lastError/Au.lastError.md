# Class `Au.lastError`

Gets, sets or clears the last error code of Windows API. Gets error text.

```
public static class lastError
```

##### Remarks

Many Windows API functions, when failed, set an error code. Code 0 means no error. It is stored in an internal thread-specific `int` variable. But only if the API declaration's `DllImport` attribute has `SetLastError = true`.

Some functions of this library simply call these API functions and don't throw exception when API fail. For example, most `Au.wnd` property-get functions. When failed, they return `false`/0/`null`/empty. Then you can use `Au.lastError.code` to get the error code or `Au.lastError.message` to get error text.

Most of functions set error code only when failed, and don't clear the old error code when succeeded. Therefore may need to call `Au.lastError.clear` before.

Windows API error code definitions and documentation are not included in this library. You can look for them in API function documentation on the internet.

##### Examples

```
wnd w = wnd.find("Notepag");
lastError.clear();
bool enabled = w.IsEnabled; //returns true if enabled, false if disabled or failed
if(!enabled && lastError.code != 0) { print.it(lastError.message); return; } //1400, Invalid window handle
print.it(enabled);
```

##### Inheritance

`object` → `lastError`

### Properties

`code`, `message`

### Methods

`clear`, `messageFor`