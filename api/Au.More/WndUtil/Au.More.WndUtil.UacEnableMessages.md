# Method `Au.More.WndUtil.UacEnableMessages`

Calls API `ChangeWindowMessageFilter` for each message in the list of messages. It allows processes of lower [UAC](../articles/UAC.html) integrity level to send these messages to this process.

```
public static void UacEnableMessages(params int[] messages)
```

##### Parameters

- *messages*  (`int[]`)