# Enum `Au.Triggers.TWLater`

Window events for the *later* parameter of window triggers. See `Au.Triggers.WindowTriggers.this[]`.

```
[Flags]
public enum TWLater : ushort
```

### Fields

| Name | Description |
| --- | --- |
| Active | Activated (became the foreground window). |
| Cloaked | The window has been cloaked (`Au.wnd.IsCloaked` true). |
| Destroyed | Destroyed (closed). |
| Inactive | Deactivated (lose the foreground window status). This event also occurs when closing the window, if it was active; then the window possibly is already destroyed, and the handle is invalid. |
| Invisible | Became invisible (`Au.wnd.IsVisible` false). This event also occurs when closing the window, if it was visible; then the window possibly is already destroyed, and the handle is invalid. |
| Minimized | The window has been minimized. |
| Name | Name changed. This event occurs only when the window is active. If name changed while inactive - when afterwards activated. |
| Uncloaked | The window has been uncloaked (`Au.wnd.IsCloaked` false). |
| Unminimized | The window has been restored from the minimized state. |
| Visible | Became visible (`Au.wnd.IsVisible` true). The window can be new or was temporarily hidden. The window is not actually visible if cloaked, minimized, etc. |