# Method `Au.sound.beep`

Generates sound of specified frequency and duration. Waits until it ends.

```
public static void beep(int freq, int duration, bool async = false)
```

##### Parameters

- *freq*  (`int`):
    Frequency, 37-32767 hertz.
- *duration*  (`int`):
    Duration, in milliseconds.
- *async*  (`bool`):
    Don't wait. Note: the sound ends when this process exits.