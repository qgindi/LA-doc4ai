# Constructor of `Au.More.WndSavedRect`

## Overload 1

Gets window rectangle and state for saving. Usually called when closing the window. See also `Au.More.WndSavedRect.ToString`.

```
public WndSavedRect(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Exceptions

- `Au.Types.AuWndException`:
    Failed to get rectangle, probably invalid window handle.

* * *

## Overload 2

Gets window rectangle and state for saving. Usually called when closing the window. See also `Au.More.WndSavedRect.ToString`.

```
public WndSavedRect(Window w)
```

##### Parameters

- *w*  (`Window`)

##### Exceptions

- `Au.Types.AuWndException`:
    Failed to get rectangle, probably invalid window handle.

* * *

## Overload 3

Gets window rectangle and state for saving. Usually called when closing the window. See also `Au.More.WndSavedRect.ToString`.

```
public WndSavedRect(Form form)
```

##### Parameters

- *form*  (`Form`)

##### Exceptions

- `Au.Types.AuWndException`:
    Failed to get rectangle, probably invalid window handle.