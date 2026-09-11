# Method `Au.More.WndUtil.UacEnableMessages`

Calls API `ChangeWindowMessageFilter`for each message in the list of messages.
It allows processes of lower[UAC](🔗) integrity level to send these messages to this process.

```csharp
public static void UacEnableMessages(params int[] messages)
```

##### Parameters

- *messages*  (`int[]`)