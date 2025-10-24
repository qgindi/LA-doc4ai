# Method `Au.Types.DSend.Progress`

Sets progress bar value, 0 to 100.

```
public int Progress(int percent)
```

##### Parameters

- *percent*  (`int`)

##### Returns

`int`

#### Remarks

Call this method while the dialog is open, eg in an event handler. Sends message `Au.Types.DNative.TDM.SET_PROGRESS_BAR_POS`.