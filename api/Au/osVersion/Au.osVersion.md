# Class `Au.osVersion`

Provides Windows version info. Also some info about the current process (eg 32/64 bit) and this library.

```
public static class osVersion
```

##### Remarks

The Windows version properties return the true Windows version; it does not depend on manifest etc.

##### Inheritance

`object` → `osVersion`

### Fields

`win10`, `win7`, `win8`, `win8_1`

### Properties

`is32BitOS`, `is32BitProcess`, `is32BitProcessAnd64BitOS`, `isArm64OS`, `isArm64Process`, `minWin10`, `minWin10_1607`, `minWin10_1703`, `minWin10_1709`, `minWin10_1803`, `minWin10_1809`, `minWin10_1903`, `minWin10_1909`, `minWin10_2004`, `minWin10_20H2`, `minWin10_21H1`, `minWin10_21H2`, `minWin10_22H2`, `minWin11`, `minWin11_22H2`, `minWin11_23H2`, `minWin11_24H2`, `minWin11_25H2`, `minWin8`, `minWin8_1`, `onaString`, `thisLibrary`, `winBuild`, `winMajor`, `winMinor`, `winVer`

### See Also

`System.OperatingSystem`

`System.Runtime.InteropServices.RuntimeInformation`