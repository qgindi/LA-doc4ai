# Class `Au.More.PrePostBuild`

Contains compilation info passed to current `preBuild`/`postBuild` script.

```csharp
public record PrePostBuild : IEquatable<PrePostBuild>
```

##### Examples

```csharp
/*/ role editorExtension; /*/
var c = PrePostBuild.Info;
print.it(c);
print.it(c.outputFile);
```

##### Inheritance

`object` → `PrePostBuild`

### Constructors

`PrePostBuild(string, string, string, string, bool, string, bool, bool)`

### Properties

`Info`, `optimize`, `outputFile`, `outputPath`, `platform`, `preBuild`, `publish`, `role`, `source`