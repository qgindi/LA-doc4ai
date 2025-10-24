# Method `Au.More.SecurityUtil.SetPrivilege`

Enables or disables a privilege for this process.

```
public static bool SetPrivilege(string privilegeName, bool enable, string computer = null)
```

##### Parameters

- *privilegeName*  (`string`)
- *enable*  (`bool`)
- *computer*  (`string`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.