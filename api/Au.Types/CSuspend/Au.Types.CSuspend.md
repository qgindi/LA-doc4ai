# Enum `Au.Types.CSuspend`

Used with `Au.computer.suspend`.

```
public enum CSuspend
```

### Fields

| Name | Description |
| --- | --- |
| Display | Turn off display. It should activate Modern Suspend S0 if available. |
| Hibernate | Hibernate. |
| Sleep | Sleep (power state S1-S3). If these power states unavailable, the function may hibernate instead. |
| SleepOrDisplay | Sleep if power states S1-S3 available, else turn off display (it should activate Modern Suspend S0 if available). |