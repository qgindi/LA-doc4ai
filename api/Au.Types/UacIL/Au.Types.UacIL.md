# Enum `Au.Types.UacIL`

UAC integrity level. See `Au.uacInfo.IntegrityLevel`.

```
public enum UacIL
```

### Fields

| Name | Description |
| --- | --- |
| High | Most rights. Processes that run as administrator. |
| Low | Very limited rights. Used by web browser tab processes, Windows Store apps. |
| Medium | Limited rights. Most processes (unless UAC turned off). |
| Protected | Undocumented. Rare. |
| System | Almost all rights. Services, some system processes. |
| UIAccess | Medium IL + can access/automate High IL windows (user interface). |
| Unknown | Failed to get IL. Unlikely. |
| Untrusted | The most limited rights. Rare. |