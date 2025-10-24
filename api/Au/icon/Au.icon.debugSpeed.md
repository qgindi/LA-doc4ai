# Property `Au.icon.debugSpeed`

If not 0, "get icon" functions of this class will print (in editor's output) their execution time in milliseconds when it >= this value.

```
public static int debugSpeed { get; set; }
```

##### Property Value

`int`

#### Remarks

Icons are mostly used in toolbars and menus. Getting icons of some files can be slow. For example if antivirus program scans the file. Toolbars and menus that use slow icons may start with a noticeable delay. Use this property to find too slow icons. Then you can replace them with fast icons, for example `.ico` files.