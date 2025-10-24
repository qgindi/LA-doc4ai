# Method `Au.clipboardData.SetClipboard`

Copies the added data of all formats to the clipboard.

```
public void SetClipboard()
```

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry) or set clipboard data.
- `OutOfMemoryException`:
    Failed to allocate memory for clipboard data.

#### Remarks

Calls API `OpenClipboard`, `EmptyClipboard`, `SetClipboardData` and `CloseClipboard`.