# Struct `Au.wnd`

A variable of `wnd` type represents a window or control. It is a window handle, also known as `HWND`.

```
public struct wnd : IEquatable<wnd>, IComparable<wnd>
```

##### Remarks

`wnd` functions can be used with windows and controls of any process/thread. Also can be used with .NET form/control and WPF window class variables, like `wnd w=form.Hwnd(); w.Method(...);`.

There are two main types of windows - top-level windows and controls. Controls are child windows of top-level windows.

More window functions are in types named like `WndX`, in namespace `Au.More`. They are used mostly in programming, rarely in automation scripts.

What happens when a `wnd` member function fails:

- Functions that get window properties don't throw exceptions. They return `false`/0/`null`/empty. Most of them support `Au.lastError`, and it is mentioned in function documentation.
- Many functions that change window properties throw exception. Exceptions are listed in function documentation. Almost all these functions throw only `Au.Types.AuWndException`.
- Other functions that change window properties return `false`. They are more often used in programming than in automation scripts.
- When a "find" function does not find the window or control, it returns `default(wnd)` (window handle 0). Then `Au.wnd.Is0` will return `true`.
- If a function does not follow these rules, it is mentioned in function documentation.

Many functions fail if the window's process has a higher [UAC](../articles/UAC.html) integrity level (administrator, uiAccess) than this process, unless this process has uiAccess level. Especially the functions that change window properties. Some functions that still work: `Activate`, `ActivateL`, `ShowMinimized`, `ShowNotMinimized`, `ShowNotMinMax`, `Close`.

The `wnd` type can be used with native Windows API functions without casting. Use `wnd` for the parameter type in the declaration, like `[DllImport(...)] static extern bool NativeFunction(wnd hWnd, ...)`.

See also: [Window Features](https://www.google.com/search?q=Window+Features+site:microsoft.com).

##### Examples

```
wnd w = wnd.find("* - Notepad");
if(w.Is0) { print.it("window not found"); return; }
w.Activate();
wnd c = w.Child(cn: "Button");
print.it(c.Name);
```

### Constructors

`wnd(nint)`

### Properties

`ClassName`, `ClientRect`, `ClientRectInScreen`, `CommonControlType`, `ControlId`, `ControlText`, `Elm`, `ExStyle`, `Get`, `Handle`, `Is0`, `Is32Bit`, `IsActive`, `IsAlive`, `IsChild`, `IsCloaked`, `IsCloakedGetState`, `IsConsole`, `IsFocused`, `IsFullScreen`, `IsHung`, `IsHungGhost`, `IsMaximized`, `IsMessageOnly`, `IsMinimized`, `IsOfThisProcess`, `IsOfThisThread`, `IsPopupWindow`, `IsResizable`, `IsToolWindow`, `IsTopmost`, `IsUnicode`, `IsUwpApp`, `IsVisible`, `IsVisibleAndNotCloaked`, `IsWindows8MetroStyle`, `MouseClientXY`, `Name`, `NameElm`, `NameWinforms`, `ProcessId`, `ProgramDescription`, `ProgramName`, `ProgramPath`, `Prop`, `Rect`, `RectInDirectParent`, `RectInWindow`, `Screen`, `Style`, `TaskbarButton`, `ThreadId`, `Uac`, `UacAccessDenied`, `Window`, `active`, `focused`

### Methods

`Activate`, `ActivateL`, `ButtonClick`, `ButtonClick`, `Child`, `Child`, `ChildAll`, `ChildFast`, `ChildFast`, `ChildFromXY`, `ChildFromXY`, `ClassNameIs`, `ClassNameIs`, `Close`, `CompareTo`, `ContainsScreenXY`, `ContainsWindowXY`, `ContainsWindowXY`, `Enable`, `EnsureInScreen`, `Equals`, `Equals`, `Equals`, `Focus`, `GetClientRect`, `GetHashCode`, `GetRect`, `GetRectIn`, `GetRectNotMinMax`, `GetText`, `GetThreadProcessId`, `GetTransparency`, `GetWindowAndClientRectInScreen`, `GetWindowLong`, `HasChild`, `HasElm`, `HasExStyle`, `HasStyle`, `IsChildOf`, `IsEnabled`, `IsMatch`, `IsMatch`, `IsOwnedBy`, `MapClientToClientOf`, `MapClientToClientOf`, `MapClientToScreen`, `MapClientToScreen`, `MapClientToWindow`, `MapClientToWindow`, `MapScreenToClient`, `MapScreenToClient`, `MapWindowToClient`, `MapWindowToClient`, `MapWindowToScreen`, `MapWindowToScreen`, `MenuClick`, `Move`, `Move`, `MoveInScreen`, `MoveL`, `MoveL`, `MoveL`, `MoveToScreenCenter`, `NameIs`, `Post`, `ProgramNameIs`, `Resize`, `ResizeClient`, `ResizeL`, `Send`, `Send`, `Send`, `SendNotify`, `SendTimeout`, `SendTimeout`, `SendTimeout`, `SetExStyle`, `SetStyle`, `SetText`, `SetTransparency`, `SetWindowLong`, `SetWindowPos`, `Show`, `ShowL`, `ShowMaximized`, `ShowMinimized`, `ShowNotMinMax`, `ShowNotMinimized`, `ThrowIf0`, `ThrowIfInvalid`, `ThrowNoNative`, `ThrowUseNative`, `ThrowUseNative`, `ThrowUseNative`, `ThrowUseNative`, `ToString`, `WaitForClosed`, `WaitForName`, `WaitFor<T>`, `ZorderAbove`, `ZorderBelow`, `ZorderBottom`, `ZorderIsAbove`, `ZorderNoTopmost`, `ZorderTop`, `ZorderTopmost`, `find`, `find`, `findAll`, `findFast`, `findOrRun`, `fromMouse`, `fromXY`, `fromXY`, `runAndFind`, `switchActiveWindow`, `wait`, `waitAny`

### Operators

`operator ==(wnd, wnd)`, `explicit operator int(wnd)`, `explicit operator nint(wnd)`, `explicit operator wnd(int)`, `explicit operator wnd(nint)`, `implicit operator wnd(SpecHWND)`, `operator !=(wnd, wnd)`