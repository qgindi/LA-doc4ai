# Method `Au.dialog.Progress`

Sets progress bar.

```
public dialog Progress(bool show, bool marquee = false)
```

##### Parameters

- *show*  (`bool`):
    Whether to show progress bar.
- *marquee*  (`bool`):
    Show just an animation that does not indicate a progress.

##### Returns

`Au.dialog`

#### Remarks

To start or stop the marquee animation, use code like this when the dialog is visible: `d.Send.Message(DNative.TDM.SET_PROGRESS_BAR_MARQUEE, 1);`. To set progress, use `Au.Types.DSend.Progress` when the dialog is visible. Example in `Au.dialog.showProgress`.