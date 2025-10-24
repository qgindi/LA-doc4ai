# Enum `Au.Triggers.TMMove`

Mouse movement directions for mouse move triggers.

```
public enum TMMove : byte
```

##### Remarks

To activate a mouse move trigger, the user quickly moves the mouse pointer to the specified direction and back. The screen is divided into 3 parts: 1 - center 50%; 2 - left or top 25%; 3 - right or bottom 25%. Constants like `UpDownInCenter50` specify a direction and screen part; the trigger works only in that screen part. Constants like `UpDown` specify just a direction; the trigger works in whole screen.

### Fields

| Name | Description |
| --- | --- |
| DownUp |  |
| DownUpInCenter50 |  |
| DownUpInLeft25 |  |
| DownUpInRight25 |  |
| LeftRight |  |
| LeftRightInBottom25 |  |
| LeftRightInCenter50 |  |
| LeftRightInTop25 |  |
| RightLeft |  |
| RightLeftInBottom25 |  |
| RightLeftInCenter50 |  |
| RightLeftInTop25 |  |
| UpDown |  |
| UpDownInCenter50 |  |
| UpDownInLeft25 |  |
| UpDownInRight25 |  |