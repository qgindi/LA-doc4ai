# Method `Au.dialog.ThreadWaitForOpen`

Can be used by other threads to wait until the dialog is open.

```
public bool ThreadWaitForOpen()
```

##### Returns

`bool`

- `true` - the dialog is open and you can send messages to it.
- `false` - the dialog is already closed or failed to show.