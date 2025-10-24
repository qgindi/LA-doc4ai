# File properties - `resource` (button **Resource**)

Add image etc file(s) as managed resources. Meta comment `/*/ resource File; /*/`.

Default resource type is `Stream`. You can append `/byte[]` or `/string`, like `/*/ resource file.txt /string; /*/`. Or `/strings`, to add multiple strings from a 2-column CSV file (name, value). Or `/embedded`, to add as a separate top-level stream that can be loaded with `Assembly.GetManifestResourceStream` (others are in top-level stream `AssemblyName.g.resources`).

The file must be in this workspace. Import files if need (eg drag-drop). Can be a link.
 If folder, will add all its descendant files.
 The value can be:

- Path in the workspace. Examples: `\File.png`, `\Folder\File.png`.
- Path relative to this file. Examples: `Folder\File.png`, `.\File.png`, `..\Folder\File.png`.
- Filename. Error if multiple exist, unless single exists in the same folder.

To remove this meta comment, edit the code.

To load resources at run time can be used class `Au.More.ResourceUtil`, like `var s = ResourceUtil.GetString("file.txt");`. Or `ResourceManager`. To load WPF resources can be used `"pack:..."` URI; if role `miniProgram`, assembly name is like `*ScriptName`.

Resource names in assembly by default are like `file.png`. When adding a folder with subfolders, may be path relative to that folder, like `subfolder/file.png`. If need path relative to this C# file, append space and `/path`. Resource names are lowercase, except `/embedded` and `/strings`. LibreAutomate does not URL-encode resource names; WPF `pack:...` URI does not work if resource name contains spaces, non-ASCII or other URL-unsafe characters. Also LibreAutomate does not convert XAML to BAML.

To browse .NET assembly resources, types, etc can be used for example [ILSpy](https://www.google.com/search?q=ILSpy).