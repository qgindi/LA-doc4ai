# File properties - `sign`

Strong-name signing key file, to sign the output assembly.

The file must be in this workspace. Import files if need (eg drag-drop). Can be a link. The value can be:

- Path in the workspace. Examples: `\App.snk`, `\Folder\App.snk`.
- Path relative to this file. Examples: `Folder\App.snk`, `.\App.snk`, `..\Folder\App.snk`.
- Filename. Error if multiple exist, unless single exists in the same folder.