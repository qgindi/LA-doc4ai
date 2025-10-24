# Method `Au.sound.speak`

Speaks text.

```
public static void speak(string text, bool async = false, string voice = null, int rate = 0, int volume = 100)
```

##### Parameters

- *text*  (`string`):
    Text to speak. If `null`, stops speaking.
- *async*  (`bool`):
    Don't wait. Note: the sound ends when this process exits.
- *voice*  (`string`):
    A voice name from **Control Panel > Speech > Text to speech**. Can be partial, case-insensitive. Example: `"Zira"`. If `null`, uses default voice. Voice attributes can be specified using string format `"voice|reqAttr"` or `"voice|reqAttr|optAttr"`. Here *reqAttr* and *optAttr* are arguments for `ISpObjectTokenCategory.EnumTokens`. Each part can be empty. Example: `"|Gender=Female"`.
- *rate*  (`int`):
    Speed adjustment, +- 10.
- *volume*  (`int`):
    Volume, 0-100. See also `Au.sound.volume`.

### See Also

`Au.More.SpeakVoice`