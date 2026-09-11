# Method `Au.keys.more.KModToWinforms`

Converts modifier key flags from `KMod` to winforms `Keys`.

```csharp
public static Keys KModToWinforms(KMod mod)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
  Enum: Shift, Ctrl, Alt, Win.

##### Returns

`Keys`

#### Remarks

For `Win` returns flag `(Keys)0x80000`.