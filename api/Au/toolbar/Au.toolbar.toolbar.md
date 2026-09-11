# Constructor of `Au.toolbar`

```csharp
public toolbar(string name = null, TBCtor flags = 0, string f_ = null, int l_ = 0, string m_ = null, string settingsFile = null)
```

##### Parameters

- *name*  (`string`):
  Toolbar name. Must be valid filename.
  Used for: toolbar window name, settings file name,`Au.toolbar.find`, some other functions.
  If`null`, uses the caller function's name if available, else exception.
- *flags*  (`Au.Types.TBCtor`):
  Enum: ResetSettings, DontSaveSettings.
- *f_*  (`string`):
  [Caller info parameter](🔗)
- *l_*  (`int`):
  [Caller info parameter](🔗)
- *m_*  (`string`):
  [Caller info parameter](🔗)
- *settingsFile*  (`string`):
  `null` or full path of the settings file of this toolbar.

##### Exceptions

- `ArgumentException`:
  Invalid *name*.

#### Remarks

Each toolbar has a settings file, where are saved its position, size and context menu settings. This function reads the file if exists, ie if settings changed in the past. See `Au.toolbar.getSettingsFilePath`. If fails, prints a warning and uses default settings.

Sets properties:

- `Au.Types.MTBase.ActionThread` = `true`.
- `Au.Types.MTBase.ExtractIconPathFromCode` = `true`.