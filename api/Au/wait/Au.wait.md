# Class `Au.wait`

Contains functions to wait for a custom condition, handle, etc, or simply sleep.

```
public static class wait
```

##### Remarks

Specialized "wait for" functions are in other classes, for example `Au.wnd.wait`.

All "wait for" functions have a timeout parameter. It is the maximal time to wait, in seconds. If 0, waits indefinitely. If `>` 0, throws `System.TimeoutException` when timed out. If \< 0, then stops waiting and returns default value of that type (`false`, etc).

While waiting, most functions by default don't dispatch Windows messages, events, hooks, timers, COM/RPC, etc. For example, if used in a `Window`/`Form`/`Control` event handler, the window would stop responding. Use another thread, for example `async`/`await`/`Task`, like in the example. Or `Au.Types.Seconds.DoEvents`.

##### Examples

```
wait.until(0, () => keys.isScrollLock);
print.it("ScrollLock now is toggled");
```

Using in a WPF window with async/await.

```
using System.Windows;
var b = new wpfBuilder("Window").WinSize(250);
b.R.AddButton("Wait", async _ => {
	  print.it("waiting for ScrollLock...");
	  var result = await Task.Run(() => wait.until(-10, () => keys.isScrollLock));
	  print.it(result);
});
if (!b.ShowDialog()) return;
```

##### Inheritance

`object` → `wait`

### Methods

`doEvents`, `doEvents`, `doEventsUntil`, `forHandle`, `forPostedMessage`, `ms`, `retry`, `retry<T>`, `s`, `s`, `until<T>`