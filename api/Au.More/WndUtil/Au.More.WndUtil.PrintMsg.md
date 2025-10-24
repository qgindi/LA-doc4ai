# Method `Au.More.WndUtil.PrintMsg`

## Overload 1

Writes a Windows message to a string. If the message is specified in *options*, sets `s=null` and returns `false`.

```
public static bool PrintMsg(out string s, wnd w, int msg, nint wParam, nint lParam, PrintMsgOptions options = null, string m_ = null)
```

##### Parameters

- *s*  (`string`)
- *w*  (`Au.wnd`)
- *msg*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)
- *options*  (`Au.Types.PrintMsgOptions`)
- *m_*  (`string`)

##### Returns

`bool`

* * *

## Overload 2

Writes a Windows message to the output, unless it is specified in *options*.

```
public static void PrintMsg(wnd w, int msg, nint wParam, nint lParam, PrintMsgOptions options = null, string m_ = null)
```

##### Parameters

- *w*  (`Au.wnd`)
- *msg*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)
- *options*  (`Au.Types.PrintMsgOptions`)
- *m_*  (`string`)

* * *

## Overload 3

Writes a Windows message to a string. If the message is specified in *options*, sets `s=null` and returns `false`.

```
public static bool PrintMsg(out string s, in MSG m, PrintMsgOptions options = null, string m_ = null)
```

##### Parameters

- *s*  (`string`)
- *m*  (`Au.Types.MSG`)
- *options*  (`Au.Types.PrintMsgOptions`)
- *m_*  (`string`)

##### Returns

`bool`

#### Remarks

The *m* parameter also accepts `System.Windows.Interop.MSG` (WPF) and `System.Windows.Forms.Message`.

* * *

## Overload 4

Writes a Windows message to the output, unless it is specified in *options*.

```
public static void PrintMsg(in MSG m, PrintMsgOptions options = null, string m_ = null)
```

##### Parameters

- *m*  (`Au.Types.MSG`)
- *options*  (`Au.Types.PrintMsgOptions`)
- *m_*  (`string`)

#### Remarks

The *m* parameter also accepts `System.Windows.Interop.MSG` (WPF) and `System.Windows.Forms.Message`.