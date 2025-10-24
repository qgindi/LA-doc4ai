# Method `Au.More.Math2.MakeLparam`

## Overload 1

Creates `uint` by placing `(ushort)loWord` in bits 1-16 and `(ushort)hiWord` in bits 17-32. Like C macro `MAKELONG`, `MAKEWPARAM`, `MAKELPARAM`, `MAKELRESULT`.

```
public static nint MakeLparam(int loWord, int hiWord)
```

##### Parameters

- *loWord*  (`int`)
- *hiWord*  (`int`)

##### Returns

`nint`

The return value is of type `nint`. It can be used with Windows message API as *lParam* or *wParam* or return value.

* * *

## Overload 2

Creates `uint` by placing `(ushort)loWord` in bits 1-16 and `(ushort)hiWord` in bits 17-32. Like C macro `MAKELONG`, `MAKEWPARAM`, `MAKELPARAM`, `MAKELRESULT`.

```
public static nint MakeLparam(uint loWord, uint hiWord)
```

##### Parameters

- *loWord*  (`uint`)
- *hiWord*  (`uint`)

##### Returns

`nint`

The return value is of type `nint`. It can be used with Windows message API as *lParam* or *wParam* or return value.

* * *

## Overload 3

Creates `uint` by placing `(ushort)p.x` in bits 1-16 and `(ushort)p.y` in bits 17-32. Like C macro `MAKELONG`, `MAKEWPARAM`, `MAKELPARAM`, `MAKELRESULT`.

```
public static nint MakeLparam(POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`)

##### Returns

`nint`

The return value is of type `nint`. It can be used with Windows message API as *lParam* or *wParam* or return value.