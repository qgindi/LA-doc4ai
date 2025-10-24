# Property `Au.Types.HookData.ThreadCbt.ActivationInfo`

Gets `Au.Types.HookData.CbtEvent.ACTIVATE` event info.

```
public HookData.ThreadCbt.CBTACTIVATESTRUCT* ActivationInfo { get; }
```

##### Exceptions

- `InvalidOperationException`:
    `Au.Types.HookData.ThreadCbt.code` is not `Au.Types.HookData.CbtEvent.ACTIVATE`.

##### Property Value

`Au.Types.HookData.ThreadCbt.CBTACTIVATESTRUCT*`