# Enum `Au.Triggers.TMEdge`

Screen edge for mouse edge triggers.

```
public enum TMEdge : byte
```

##### Remarks

To activate a screen edge trigger, the user touches a screen edge with the mouse pointer. Each screen edge is divided into 3 parts: 1 - center 50%; 2 - left or top 25%; 3 - right or bottom 25%. Constants like `TopInCenter50` specify an edge and part; the trigger works only in that part of that edge. Constants like `Top` specify just an edge; the trigger works in all parts of that edge.

### Fields

| Name | Description |
| --- | --- |
| Bottom |  |
| BottomInCenter50 |  |
| BottomInLeft25 |  |
| BottomInRight25 |  |
| Left |  |
| LeftInBottom25 |  |
| LeftInCenter50 |  |
| LeftInTop25 |  |
| Right |  |
| RightInBottom25 |  |
| RightInCenter50 |  |
| RightInTop25 |  |
| Top |  |
| TopInCenter50 |  |
| TopInLeft25 |  |
| TopInRight25 |  |