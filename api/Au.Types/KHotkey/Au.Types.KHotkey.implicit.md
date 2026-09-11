# Operator `Au.Types.KHotkey.implicit operator`

## Overload 1

Implicit conversion from string like `"Ctrl+Shift+K"`.

```csharp
public static implicit operator KHotkey(string hotkey)
```

##### Parameters

- *hotkey*  (`string`)

##### Returns

`Au.Types.KHotkey`

##### Exceptions

- `ArgumentException`:
  Error in hotkey.

* * *

## Overload 2

Implicit conversion from tuple `(KMod, KKey)`.

```csharp
public static implicit operator KHotkey((KMod, KKey) hotkey)
```

##### Parameters

- *hotkey*  (`(KMod, KKey)`)

##### Returns

`Au.Types.KHotkey`

* * *

## Overload 3

Implicit conversion from `Au.Types.KKey` (hotkey without modifiers).

```csharp
public static implicit operator KHotkey(KKey key)
```

##### Parameters

- *key*  (`Au.Types.KKey`)

##### Returns

`Au.Types.KHotkey`

* * *

## Overload 4

Implicit conversion from `System.Windows.Forms.Keys` like `Keys.Ctrl|Keys.B`.

```csharp
public static implicit operator KHotkey(Keys hotkey)
```

##### Parameters

- *hotkey*  (`Keys`)

##### Returns

`Au.Types.KHotkey`