# Method `Au.wnd.Close`

Closes the window.

```
public bool Close(bool noWait = false, bool useXButton = false)
```

##### Parameters

- *noWait*  (`bool`):
    If `true`, does not wait until the window is closed. If `false`, waits about 1 s (depends on window type etc) until the window is destroyed or disabled.
- *useXButton*  (`bool`):
    If `false` (default), uses API message `WM_CLOSE`. If `true`, uses API message [WM_SYSCOMMAND SC_CLOSE](https://www.google.com/search?q=WM_SYSCOMMAND+SC_CLOSE+site:microsoft.com), like when the user clicks the `X` button in the title bar. Most windows can be closed with any of these messages, but some respond properly only to one of them. For example, some applications on `WM_CLOSE` don't exit, although the main window is closed. Some applications don't respond to `WM_SYSCOMMAND` if it is posted soon after opening the window.

##### Returns

`bool`

`true` if successfully closed or if it was already closed (the handle is 0 or invalid) or if *noWait*==`true`.

#### Remarks

The window may refuse to be closed. For example, it may be hung, or hide itself instead, or display a "Save?" message box, or is a dialog without `X` button, or just need more time to close it. If the window is of this thread, just calls `Au.wnd.Send` or `Au.wnd.Post` (if *noWait*==`true`) and returns `true`.

#### Examples

```
//close all Notepad windows
foreach (var w in wnd.findAll("* Notepad", "Notepad")) w.Close();
```

### See Also

`Au.wnd.WaitForClosed`