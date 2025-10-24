# Method `Au.Types.ExtWpf.DpiChangedWorkaround`

## Overload 1

Workaround for WPF bug: on DPI change tries to activate window. Call on `WM_DPICHANED` message or in `OnDpiChanged` override.

```
public static void DpiChangedWorkaround(this Window t)
```

##### Parameters

- *t*  (`Window`)

* * *

## Overload 2

Workaround for WPF bug: on DPI change tries to activate window. Call on `WM_DPICHANED` message or in `OnDpiChanged` override. Only if top-level window.

```
public static void DpiChangedWorkaround(this HwndSource t)
```

##### Parameters

- *t*  (`HwndSource`)