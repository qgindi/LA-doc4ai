# Method `Au.sound.playWav`

Plays a custom sound (`.wav` file).

```
public static bool playWav(string wavFile, bool async = false, bool system = false)
```

##### Parameters

- *wavFile*  (`string`):
    `.wav` file.
- *async*  (`bool`):
    Don't wait until the sound ends. Note: the sound ends when this process exits.
- *system*  (`bool`):
    Use the sound volume channel "System Sounds". Then `Au.sound.volume` isn't used.

##### Returns

`bool`