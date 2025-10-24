# Enum `Au.Triggers.TMFlags`

Flags of mouse triggers.

```
[Flags]
public enum TMFlags : byte
```

### Fields

| Name | Description |
| --- | --- |
| ButtonModUp | Run the action when the mouse button and modifier keys are released. |
| LeftMod | The trigger works only with left-side modifier keys. |
| RightMod | The trigger works only with right-side modifier keys. |
| ShareEvent | Allow other apps to receive the mouse button or wheel message too. Used only with the click and wheel triggers. To receive and block mouse messages is used a low-level hook. Other hooks may receive blocked messages or not, depending on when they were set. |