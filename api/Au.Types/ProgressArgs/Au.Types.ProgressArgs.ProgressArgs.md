# Constructor of `Au.Types.ProgressArgs`

```
public ProgressArgs(long Total, long Current, int Percent)
```

##### Parameters

- *Total*  (`long`):
    The max expected value. Or 0 if unknown.
- *Current*  (`long`):
    The current value.
- *Percent*  (`int`):
    `Current * 100 / Total`. Or 0 if unknown.