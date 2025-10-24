# Method `Au.dialog.ShowDialogNoWait`

Shows the dialog in new thread and returns without waiting until it is closed.

```
public void ShowDialogNoWait()
```

##### Exceptions

- `Win32Exception`:
    Failed to show dialog. Unlikely.

#### Remarks

Calls `Au.dialog.ThreadWaitForOpen`, therefore the dialog is already open when this function returns. More info: `Au.dialog.showNoWait`