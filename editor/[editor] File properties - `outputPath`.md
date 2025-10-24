# File properties - `outputPath`

Directory for the output assembly file and related files (used dlls, etc).

Full path. Can start with `%environmentVariable%` or `%folders.SomeFolder%` (see class `Au.folders`). Can be path relative to this file or workspace, like with other properties.

Default if role `exeProgram`: `%folders.Workspace%\exe\filename`. Default if role `classLibrary`: `%folders.Workspace%\dll`. The compiler creates the folder if does not exist.