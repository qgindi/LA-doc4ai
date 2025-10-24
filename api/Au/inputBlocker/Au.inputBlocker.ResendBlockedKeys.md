# Property `Au.inputBlocker.ResendBlockedKeys`

Record blocked keys, and play back when stopped blocking.

```
public bool ResendBlockedKeys { get; set; }
```

##### Property Value

`bool`

#### Remarks

Will not play back if: 1. The blocking time is > 10 seconds; then plays back only key-up events. 2. Detected `Ctrl+Alt+Delete`, [UAC](../articles/UAC.html) consent or some other special screen. 3. Called `Au.inputBlocker.Pause`.