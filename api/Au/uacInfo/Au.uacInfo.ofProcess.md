# Method `Au.uacInfo.ofProcess`

Opens process access token and creates/returns new `Au.uacInfo` variable that holds it. Then you can use its properties.

```
public static uacInfo ofProcess(int processId)
```

##### Parameters

- *processId*  (`int`):
    Process id. If you have a window, use `Au.wnd.ProcessId`.

##### Returns

`Au.uacInfo`

`null` if failed. For example fails for services and some other processes if current process is not administrator.

#### Remarks

To get `Au.uacInfo` of this process, use `Au.uacInfo.ofThisProcess`.