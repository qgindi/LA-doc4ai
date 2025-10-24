# File properties - `manifest`

[manifest file](https://www.google.com/search?q=site:microsoft.com+manifest+file) of the output exe file.

The file must be in this workspace. Import files if need (eg drag-drop). Can be a link. The value can be:

- Path in the workspace. Examples: `\App.manifest`, `\Folder\App.manifest`.
- Path relative to this file. Examples: `Folder\App.manifest`, `.\App.manifest`, `..\Folder\App.manifest`.
- Filename. Error if multiple exist, unless single exists in the same folder.

The manifest will be added as a native resource.