# Method `Au.process.getSessionId`

Gets user session id of a process (API `ProcessIdToSessionId`).

```
public static int getSessionId(int processId)
```

##### Parameters

- *processId*  (`int`):
    Process id.

##### Returns

`int`

Returns -1 if failed. Supports `Au.lastError`.