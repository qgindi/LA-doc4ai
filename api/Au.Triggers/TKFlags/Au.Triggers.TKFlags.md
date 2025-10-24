# Enum `Au.Triggers.TKFlags`

Flags of hotkey triggers.

```
[Flags]
public enum TKFlags
```

### Fields

| Name | Description |
| --- | --- |
| ExtendedNo | The key must not be an "extended key". See `Au.Types.KKeyScan` example code. Don't use this flag with `NumpadX` flags. |
| ExtendedYes | The key must be an "extended key". See `Au.Types.KKeyScan` example code. Don't use this flag with `NumpadX` flags. |
| KeyModUp | Run the action when the key and modifier keys are released. |
| LeftMod | The trigger works only with left-side modifier keys. |
| NoModOff | Don't release modifier keys. <br>Without this flag, for example if trigger is `["Ctrl+K"]`, when the user presses `Ctrl` and `K` down, the trigger sends `Ctrl` key-up event, making the key logically released, although it is still physically pressed. Then modifier keys don't interfere with the action. However functions like `Au.keys.getMod` and `Au.keys.waitForKey` (and any such functions in any app) will not know that the key is physically pressed; there is no API to get physical key state. <br>Other flags that prevent releasing modifier keys: `KeyUp`, `ShareEvent`. Then don't need this flag. <br>Note: Unreleased modifier keys will interfere with mouse functions like `Au.mouse.click`. Will not interfere with keyboard and clipboard functions of this library, because they release modifier keys, unless `opt.key.NoModOff` is `true`. Will not interfere with functions that send text, unless `opt.key.NoModOff` is `true` and `opt.key.TextHow` is `OKeyText.KeysX`. |
| Numpad | The trigger works only with the key that is on the numeric keypad. This flag can be used with `Enter`, `Home`, `End`, `PgUp`, `PgDown`, arrows, `Ins` and `Del`. |
| NumpadNot | The trigger works only with the key that is not on the numeric keypad. This flag can be used with `Enter`, `Home`, `End`, `PgUp`, `PgDown`, arrows, `Ins` and `Del`. |
| RightMod | The trigger works only with right-side modifier keys. |
| ShareEvent | Allow other apps to receive the key down message too. <br>Without this flag, other apps usually receive only modifier keys. Also, OS always receives `Ctrl+Alt+Delete` and some other hotkeys. <br>To receive and block key messages is used a low-level hook. Other hooks may receive blocked messages or not, depending on when they were set. |