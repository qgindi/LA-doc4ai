# Class `Au.clipboard`

Clipboard functions. Copy, paste, get and set clipboard text and other data.

```
public static class clipboard
```

##### Remarks

This class is similar to the .NET `System.Windows.Forms.Clipboard` class, which uses OLE API, works only in STA threads and does not work well in automation scripts. This class uses non-OLE API and works well in automation scripts and any threads.

To set/get clipboard data of non-text formats, use class `Au.clipboardData`; to paste, use it with `Au.clipboard.pasteData`; to copy (get from the active app), use it with `Au.clipboard.copyData<T>`.

Don't copy/paste in windows of own thread. Call it from another thread. Example in `Au.keys.send`.

##### Inheritance

`object` → `clipboard`

### Properties

`text`

### Methods

`clear`, `copy`, `copyData<T>`, `paste`, `pasteData`, `tryCopy`, `tryPaste`