# Method `Au.filesystem.exists`

Gets file or directory attributes as `Au.Types.FAttr` that tells whether it exists, is directory, readonly, hidden, system, NTFS link. See examples.

```
public static FAttr exists(string path, bool useRawPath = false)
```

##### Parameters

- *path*  (`string`):
    Full path. Supports `@"\.."` etc. If *useRawPath* is `false` (default), supports environment variables (see `Au.pathname.expand`). Can be `null`.
- *useRawPath*  (`bool`):
    Pass *path* to the API as it is, without any normalizing and full-path checking.

##### Returns

`Au.Types.FAttr`

#### Remarks

Supports `Au.lastError`. If you need exception when fails, instead call `Au.filesystem.getAttributes`. Always use full path. If not full path: if *useRawPath* is `false` (default), can't find the file; if *useRawPath* is `true`, searches in "current directory". For NTFS links gets attributes of the link, not of the target; does not care whether its target exists.

#### Examples

```
var path = @"C:\Test\test.txt";
if (filesystem.exists(path)) print.it("exists");
if (filesystem.exists(path).File) print.it("exists as file");
if (filesystem.exists(path).Directory) print.it("exists as directory");
if (filesystem.exists(path) is FAttr { File: true, IsReadonly: false }) print.it("exists as file and isn't readonly");
switch (filesystem.exists(path)) {
case 0: print.it("doesn't exist"); break;
case 1: print.it("file"); break;
case 2: print.it("directory"); break;
}
```