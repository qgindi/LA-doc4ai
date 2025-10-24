# Property `Au.wnd.getwnd.shellWindow`

Calls API `GetShellWindow`. It gets a window of the shell process (usually process `"explorer"`, class name `"Progman"`).

```
public static wnd shellWindow { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if there is no shell process, for example Explorer process killed/crashed and still not restarted, or if using a custom shell that does not register a shell window.

#### Remarks

It can be the window that contains desktop icons (see `Au.wnd.getwnd.desktop`) or other window of the same thread.