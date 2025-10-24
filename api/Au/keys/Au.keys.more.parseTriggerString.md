# Method `Au.keys.more.parseTriggerString`

Parses hotkey trigger string or mouse trigger modifiers string. Like `Au.keys.more.parseHotkeyString`, but supports "any mod" (like `"Shift?+K"` or `"?+K"`) and *noKey*.

```
public static bool parseTriggerString(string s, out KMod mod, out KMod modAny, out KKey key, bool noKey)
```

##### Parameters

- *s*  (`string`)
- *mod*  (`Au.Types.KMod`)
- *modAny*  (`Au.Types.KMod`)
- *key*  (`Au.Types.KKey`)
- *noKey*  (`bool`):
    Modifiers only. If `true`, *s* must be `"modifiers"` or `null`/`""`. If `false`, *s* must be `"key"` or `"modifiers+key"`.

##### Returns

`bool`