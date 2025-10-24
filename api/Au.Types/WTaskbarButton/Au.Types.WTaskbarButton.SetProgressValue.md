# Method `Au.Types.WTaskbarButton.SetProgressValue`

Sets the value of the progress indicator displayed on the taskbar button of this window. Calls `ITaskbarList3.SetProgressValue`.

```
public void SetProgressValue(int progressValue, int progressTotal = 100)
```

##### Parameters

- *progressValue*  (`int`):
    Progress indicator value, 0 to *progressTotal*.
- *progressTotal*  (`int`):
    Max progress indicator value.