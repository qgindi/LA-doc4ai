# Enum `Au.Types.UacElevation`

`Au.uacInfo.Elevation`.

```
public enum UacElevation
```

### Fields

| Name | Description |
| --- | --- |
| Default | Processes in this user session cannot be elevated. Can be: non-administrator user session (processes have limited rights); service session (processes have all rights); UAC is turned off (most processes have administrator rights). |
| Full | Runs as administrator (`High` or `System` integrity level, see `Au.Types.UacIL`), and UAC is not turned off. Also known as "elevated". |
| Limited | Runs as standard user (`Medium`, `UIAccess` or `Low` integrity level, see `Au.Types.UacIL`) in administrator user session (because of UAC). |
| Unknown | Failed to get. Normally it never happens. |