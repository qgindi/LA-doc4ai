# Property `Au.elm.State`

Gets UI element state (flags).

```
public EState State { get; }
```

##### Property Value

`Au.Types.EState`

0 if failed. Supports `Au.lastError`.

#### Examples

```
if(e.State.Has(EState.INVISIBLE)) print.it("has state INVISIBLE");
if(e.IsInvisible) print.it("invisible");
```