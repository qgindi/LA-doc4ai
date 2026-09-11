# Enum `Au.Types.CSLink`

See `Au.filesystem.more.createSymbolicLink`

```csharp
public enum CSLink
```

## Fields

### `Directory`

Symbolic link to directory.

### `File`

Symbolic link to file.

### `Junction`

Junction to directory.

Usually junctions work like symbolic links, but there are differences when creating them:

- Don't need admin privileges to create.
- Target must be full path. Fails if relative path.
- Target must be on this computer. Fails if on a network computer.
- Target must be directory. Fails if file.

Some programs interpret junctions differently. For example git adds the target directory.

### `JunctionOrSymlink`

Junction to local directory or symbolic link to network directory.