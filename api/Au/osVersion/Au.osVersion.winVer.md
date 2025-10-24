# Property `Au.osVersion.winVer`

Gets Windows major and minor version in single `int`: Win7 - 0x601; Win8 - 0x602; Win8.1 - 0x603; Win10/11 - 0xA00. Example: `if (osVersion.winVer >= osVersion.win8) ...`

```
public static int winVer { get; }
```

##### Property Value

`int`