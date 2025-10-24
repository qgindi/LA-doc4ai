# Method `Au.osdText.Show`

Shows the OSD window. Creates if need. By default does not wait; the window will be closed after `Au.osdText.SecondsTimeout`.

```
public override void Show()
```

##### Overrides

`Au.Types.OsdWindow.Show()`

#### Remarks

Depending on `Au.osdText.ShowMode`, creates the OSD window in this or new thread. If the OSD window is already created, just shows it if hidden. Many properties can be changed only before creating OSD window; call `Au.Types.OsdWindow.Close` if need.