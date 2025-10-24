# Constructor of `Au.More.PrePostBuild`

```
public PrePostBuild(string outputFile, string outputPath, string source, string role, bool optimize, string platform, bool preBuild, bool publish)
```

##### Parameters

- *outputFile*  (`string`):
    Full path of the output exe or dll file.
- *outputPath*  (`string`):
    Meta comment `outputPath`.
- *source*  (`string`):
    Path of this C# code file in the workspace.
- *role*  (`string`):
    Meta comment `role`.
- *optimize*  (`bool`):
    Meta comment `optimize`.
- *platform*  (`string`):
    Meta comment `platform`.
- *preBuild*  (`bool`):
    `true` if the script used with meta `preBuild`, `false` if with `postBuild`.
- *publish*  (`bool`):
    `true` when publishing.