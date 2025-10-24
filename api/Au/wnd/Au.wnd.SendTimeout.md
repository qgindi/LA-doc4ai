# Method `Au.wnd.SendTimeout`

## Overload 1

Calls/returns API `SendMessageTimeout` and gets the result of the message processing.

```
public bool SendTimeout(int millisecondsTimeout, out nint result, int message, nint wParam = 0, nint lParam = 0, SMTFlags flags = SMTFlags.ABORTIFHUNG)
```

##### Parameters

- *millisecondsTimeout*  (`int`)
- *result*  (`nint`)
- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)
- *flags*  (`Au.Types.SMTFlags`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

* * *

## Overload 2

Calls/returns API `SendMessageTimeout` where *lParam* is string.

```
public bool SendTimeout(int millisecondsTimeout, out nint result, int message, nint wParam, string lParam, SMTFlags flags = SMTFlags.ABORTIFHUNG)
```

##### Parameters

- *millisecondsTimeout*  (`int`)
- *result*  (`nint`)
- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`string`)
- *flags*  (`Au.Types.SMTFlags`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

* * *

## Overload 3

Calls/returns API `SendMessageTimeout` and gets the result of the message processing.

```
public bool SendTimeout(int millisecondsTimeout, out nint result, int message, nint wParam, void* lParam, SMTFlags flags = SMTFlags.ABORTIFHUNG)
```

##### Parameters

- *millisecondsTimeout*  (`int`)
- *result*  (`nint`)
- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`void*`)
- *flags*  (`Au.Types.SMTFlags`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.