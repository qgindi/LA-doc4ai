# Method `Au.More.WndSavedRect.Restore`

## Overload 1

Calls `Au.More.WndSavedRect.FromString`. If it returns `true`, calls `Au.More.WndSavedRect.NormalizeRect`, `Au.Types.ExtWpf.SetRect`, maximizes if need and returns `true`. Call this function before showing window.

```
public static bool Restore(Window w, string saved, Action<string> save = null)
```

##### Parameters

- *w*  (`Window`)
- *saved*  (`string`):
    String created by `Au.More.WndSavedRect.ToString`.
- *save*  (`Action<string>`):
    If not `null`, called when closing the window. Receives string for saving. Can save it in registry, file, anywhere.

##### Returns

`bool`

##### Exceptions

- `InvalidOperationException`:
    Window is loaded.

* * *

## Overload 2

Calls `Au.More.WndSavedRect.FromString`. If it returns `true`, sets *form* bounds = `Au.More.WndSavedRect.NormalizeRect`, maximizes if need, sets `StartPosition` = `Manual`, and returns `true`. Call this function before showing window.

```
public static bool Restore(Form form, string saved, Action<string> save = null)
```

##### Parameters

- *form*  (`Form`)
- *saved*  (`string`):
    String created by `Au.More.WndSavedRect.ToString`.
- *save*  (`Action<string>`):
    If not `null`, called when closing the window. Receives string for saving. Can save it in registry, file, anywhere.

##### Returns

`bool`