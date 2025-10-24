# File properties - `icon`

Icon of the output exe file.

The icon will be added as a native resource and displayed in File Explorer etc. Native resources can be used with `Au.icon.ofThisApp` etc and `Au.dialog` class functions.

The file must be in this workspace. Import files if need (eg drag-drop). Can be a link. The value can be:

- Path in the workspace. Examples: `\App.ico`, `\Folder\App.ico`.
- Path relative to this file. Examples: `Folder\App.ico`, `.\App.ico`, `..\Folder\App.ico`.
- Filename. Error if multiple exist, unless single exists in the same folder.

If role `exeProgram`, you can specify a folder instead. Will add all `.ico` and `.xaml` icons from it. Resource ids start from `IDI_APPLICATION` (32512).

Another way to set exe icon - assign a custom icon to the main C# file. See menu **Tools > Icons**.