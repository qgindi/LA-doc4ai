# Method `Au.wnd.Show`

Shows (if hidden) or hides this window.

```
public void Show(bool show)
```

##### Parameters

- *show*  (`bool`)

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

Does not activate/deactivate/zorder. This window can be of any thread. If you know it is of this thread, use `Au.wnd.ShowL`. This function calls it.