# Method `Au.More.WndCopyData.EnableReceivingWM_COPYDATA`

Calls API `ChangeWindowMessageFilter`(`WM_COPYDATA`). Then windows of this process can receive this message from lower [UAC](../articles/UAC.html) integrity level processes.

```
public static void EnableReceivingWM_COPYDATA()
```