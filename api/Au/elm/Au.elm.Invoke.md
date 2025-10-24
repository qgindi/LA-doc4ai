# Method `Au.elm.Invoke`

Performs the UI element's default action (see `Au.elm.DefaultAction`). Usually it is "click", "press" or similar. Like a mouse click but without moving the mouse cursor or pressing mouse buttons.

```
public void Invoke()
```

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Fails if the UI element does not have a default action. Then you can use `Au.elm.MouseClick`, or try `Au.elm.PostClick`, `Au.elm.Check`, `Au.elm.SendKeys`, other functions. The action can take long time, for example show a dialog. This function normally does not wait. It allows the caller to automate the dialog. If it waits, try `Au.elm.JavaInvoke` or one of the above functions (`Au.elm.MouseClick` etc).