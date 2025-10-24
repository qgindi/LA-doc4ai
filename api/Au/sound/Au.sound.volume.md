# Property `Au.sound.volume`

Gets or sets the sound volume of this program. Percent 0-100 of the master volume.

```
public static int volume { get; set; }
```

##### Exceptions

- `ArgumentException`

##### Property Value

`int`

#### Remarks

Used for speech and `.wav` files, but not for system sounds. Sets volume for each program seperately. The program remembers it after restarting. Note: all scripts with role *miniProgram* (default) run in the same program (`Au.Task.exe`).