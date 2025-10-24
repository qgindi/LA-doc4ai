# Property `Au.Types.PrintServerMessage.TimeUtc`

Message time in `FILETIME` format, UTC. Used with `Au.Types.PrintServerMessageType.Write`. To convert to string: `DateTime.FromFileTimeUtc(m.TimeUtc).ToLocalTime().ToString()`.

```
public long TimeUtc { get; }
```

##### Property Value

`long`