# Property `Au.Types.HookData.ThreadCbt.CreationInfo`

Gets `Au.Types.HookData.CbtEvent.CREATEWND` event info. You can modify `x`, `y`, `cx`, `cy`, and `hwndInsertAfter`.

```
public HookData.ThreadCbt.CBT_CREATEWND* CreationInfo { get; }
```

##### Exceptions

- `InvalidOperationException`:
    `Au.Types.HookData.ThreadCbt.code` is not `Au.Types.HookData.CbtEvent.CREATEWND`.

##### Property Value

`Au.Types.HookData.ThreadCbt.CBT_CREATEWND*`