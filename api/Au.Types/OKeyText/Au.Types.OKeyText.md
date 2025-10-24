# Enum `Au.Types.OKeyText`

How functions send text. See `Au.Types.OKey.TextHow`.

```
public enum OKeyText
```

##### Remarks

There are three ways to send text to the active app using keys:

- Characters (default) - use special key code `VK_PACKET`. Can send most characters.
- Keys - use virtual-key codes, with `Shift` etc where need. Can send only characters that can be simply entered with the keyboard using current keyboard layout.
- Paste - use the clipboard and `Ctrl+V`. Can send any text.

Most but not all apps support all three ways.

### Fields

| Name | Description |
| --- | --- |
| Characters | Send most text characters using special key code `VK_PACKET`. This option is default. Few apps don't support it. For newlines, tab and space sends keys (`Enter`, `Tab`, `Space`), because `VK_PACKET` often does not work well. If text contains Unicode characters with Unicode code above 0xffff, clipboard-pastes whole text, because many apps don't support Unicode surrogates sent as `WM_PACKET` pairs. |
| KeysOrChar | Send virtual-key codes, with `Shift` etc where need. All apps support it. If a character cannot be simply typed with the keyboard using current keyboard layout, sends it like with the `Characters` option. |
| KeysOrPaste | Send virtual-key codes, with `Shift` etc where need. All apps support it. If text contains characters that cannot be simply typed with the keyboard using current keyboard layout, clipboard-pastes whole text. |
| Paste | Paste text using the clipboard and `Ctrl+V`. Few apps don't support it. This option is recommended for long text, because other ways then are too slow. Other options are unreliable when text length is more than 4000 and the target app is too slow to process sent characters. Then `Au.Types.OKey.TextSpeed` can help. Also, other options are unreliable when the target app modifies typed text, for example has such features as auto-complete, auto-indent or auto-correct. However some apps modify even pasted text, for example trim the last newline or space. When pasting text, previous clipboard data of some formats is lost. Text is restored by default. |