# Method `Au.sound.playEvent`

Plays a system event sound.

```
public static bool playEvent(string name, bool async = false, bool system = false, bool orDefault = false)
```

##### Parameters

- *name*  (`string`):
    Sound event name. If `null`, displays all available names.
- *async*  (`bool`):
    Don't wait until the sound ends. Note: the sound ends when this process exits.
- *system*  (`bool`):
    Use the sound volume channel "System Sounds". Then `Au.sound.volume` isn't used.
- *orDefault*  (`bool`):
    Play default sound if the specified sound not found or does not have a `.wav` file assigned.

##### Returns

`bool`

#### Remarks

Sounds can be changed in the Control Panel's Sound dialog.