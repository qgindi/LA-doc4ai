# Class `Au.elm`

Represents a UI element. Clicks, gets properties, etc.

```
public sealed class elm : IDisposable
```

##### Remarks

UI elements are user interface (UI) parts that are accessible through programming interfaces (API). For example buttons, links, list items. This class can find them, get properties, click, etc. Web pages and most other windows support UI elements.

An `elm` variable contains a COM interface pointer (`IAccessible` or other) and uses methods of that interface or/and related API.

`elm` functions that get properties don't throw exception when the COM etc method failed (returned an error code of `HRESULT` type). Then they return `""` (string properties), 0, `false`, `null` or empty collection, depending on return type. Applications implement UI elements differently, often with bugs, and their COM interface functions return a variety of error codes. It's impossible to reliably detect whether the error code means an error or the property is merely unavailable. These `elm` functions also set the last error code of this thread = the return value (`HRESULT`) of the COM function, and callers can use `Au.lastError` to get it. If `Au.lastError.code` returns 1 (`S_FALSE`), in most cases it's not an error, just the property is unavailable. On error it will probably be a negative error code.

You can dispose `elm` variables to release the COM object, but it is not necessary (GC will do it later).

An `elm` variable cannot be used in multiple threads. Only `Dispose` can be called in any thread.

UI elements are implemented and live in their applications. This class just communicates with them. [Known UI element issues in various applications](../articles/UI%20element%20issues.html)

##### Examples

Click link `"Example"` in Chrome.

```
var w = wnd.find(0, "* Chrome");
var e = w.Elm["web:LINK", "Example"].Find(5);
e.Invoke();
```

Click a link, wait for new web page, click a link in it.

```
var w = wnd.find(0, "* Chrome");
var e = w.Elm["web:LINK", "Link 1"].Find(5);
e.WebInvoke();
w.Elm["web:LINK", "Link 2"].Find(5).WebInvoke();
```

##### Inheritance

`object` → `elm`

### Properties

`ChildCount`, `DefaultAction`, `Description`, `Elm`, `Help`, `IsChecked`, `IsChecked2`, `IsDisabled`, `IsFocused`, `IsInvisible`, `IsOffscreen`, `IsPassword`, `IsPressed`, `IsReadonly`, `IsSelected`, `Item`, `KeyboardShortcut`, `Level`, `MiscFlags`, `Name`, `Parent`, `Rect`, `Role`, `RoleInt`, `SelectedChildren`, `State`, `UiaCN`, `UiaId`, `Value`, `WndContainer`, `WndTopLevel`, `path`

### Methods

`Check`, `Check`, `ComboSelect`, `Dispose`, `Expand`, `Expand`, `Expand`, `Expand`, `Focus`, `GetProperties`, `GetRect`, `GetRect`, `Html`, `HtmlAttribute`, `HtmlAttributes`, `Invoke`, `JavaInvoke`, `MouseClick`, `MouseClickD`, `MouseClickR`, `MouseMove`, `Navigate`, `PostClick`, `PostClickD`, `PostClickR`, `ScrollTo`, `Select`, `SendKeys`, `ToString`, `WaitFor<T>`, `WebInvoke`, `focused`, `fromEvent`, `fromMouse`, `fromWindow`, `fromXY`, `fromXY`