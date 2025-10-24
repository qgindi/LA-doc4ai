# Method `Au.Types.MObject.Screen`

Allows to specify coordinates in a screen, either in the work area or in entire rectangle.

```
public static MObject Screen(screen s, bool workArea)
```

##### Parameters

- *s*  (`Au.screen`)
- *workArea*  (`bool`)

##### Returns

`Au.Types.MObject`

#### Examples

```
mouse.move(MObject.Screen(screen.primary, true), ^10, ^10); //near the bottom-right corner of the work area of the primary screen
```