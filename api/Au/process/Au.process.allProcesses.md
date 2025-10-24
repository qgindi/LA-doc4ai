# Method `Au.process.allProcesses`

Gets basic info of all processes: name, id, session id.

```
public static ProcessInfo[] allProcesses(bool ofThisSession = false)
```

##### Parameters

- *ofThisSession*  (`bool`):
    Get processes only of this user session (skip services etc).

##### Returns

`Au.Types.ProcessInfo[]`

##### Exceptions

- `Au.Types.AuException`:
    Failed. Unlikely.