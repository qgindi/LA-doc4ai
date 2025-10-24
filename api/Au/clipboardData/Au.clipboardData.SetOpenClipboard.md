# Method `Au.clipboardData.SetOpenClipboard`

Copies the added data of all formats to the clipboard which is open/owned by this thread.

```
public void SetOpenClipboard(bool renderLater = false, int format = 0)
```

##### Parameters

- *renderLater*  (`bool`):
    Call API `SetClipboardData`: `SetClipboardData(format, default)`. When/if some app will try to get clipboard data, the first time your clipboard owner window will receive `WM_RENDERFORMAT` message and should call `SetOpenClipboard(false);`.
- *format*  (`int`):
    Copy data only of this format. If 0 (default), of all formats.

##### Exceptions

- `OutOfMemoryException`:
    Failed to allocate memory for clipboard data.
- `Au.Types.AuException`:
    Failed to set clipboard data.

#### Remarks

This function is similar to `Au.clipboardData.SetClipboard`. It calls API `SetClipboardData` and does not call `OpenClipboard`, `EmptyClipboard`, `CloseClipboard`. The clipboard must be open and owned by a window of this thread.