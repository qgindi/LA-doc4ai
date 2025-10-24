# Struct `Au.More.WndCopyData`

Send/receive data to/from other process using message `WM_COPYDATA`.

```
public struct WndCopyData
```

##### Remarks

This struct is `COPYDATASTRUCT`.

> **Note:**
> By default [UAC](../articles/UAC.html) blocks messages sent from processes of lower integrity level. Call `Au.More.WndCopyData.EnableReceivingWM_COPYDATA` if need.

### Constructors

`WndCopyData(nint)`

### Properties

`DataId`, `RawData`, `RawDataSize`

### Methods

`EnableReceivingWM_COPYDATA`, `GetBytes`, `GetString`, `Return`, `Return<T>`, `SendReceive<TSend>`, `SendReceive<TSend>`, `SendReceive<TSend, TReceive>`, `Send<T>`

### See Also

`System.IO.MemoryMappedFiles.MemoryMappedFile`

`System.IO.Pipes.NamedPipeServerStream`