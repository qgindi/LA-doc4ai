# Mouse get position, wait, cursor, etc

Get mouse cursor position.

```csharp
var p = mouse.xy;
print.it(p);
```

Is mouse left button pressed?

```csharp
if (mouse.isPressed(MButtons.Left)) print.it("yes");
```

Wait for mouse left button down. [More info](🔗).

```csharp
mouse.waitForClick(0, MButtons.Left);
```

Wait for cursor (mouse pointer). [More info](🔗).

```csharp
mouse.waitForCursor(0, MCursor.Hand); //standard
mouse.waitForCursor(0, -3191259760238497114); //custom
```

Get cursor hash for `waitForCursor`.

```csharp
if(MouseCursor.GetCurrentVisibleCursor(out var c)) print.it(MouseCursor.Hash(c));
```

Also there are more `Au.mouse` class functions.