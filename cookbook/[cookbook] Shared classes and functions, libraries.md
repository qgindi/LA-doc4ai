# Shared classes and functions, libraries

Over time you'll probably create classes with functions that could be used in multiple scripts. There are 3 ways.

1. Put the classes in one or more class files. Add these class files to code files where you want to use them: in the **Properties** dialog click **Class file** and select from the list.
2. Put the classes in one or more class library projects. Add these projects to code files where you want to use them: in the **Properties** dialog click **Project** and select from the list. The library project will be compiled when need; it will create a dll file that also can be used in other workspaces, as well as in other .NET programs and libraries.
3. Put the classes in file global.cs. Or in class files added to `global.cs`. Use this only for classes that should be available in ALL code files (script, class) of current workspace. Also in `global.cs` you can add library references: in the **Properties** dialog click **Library**.

Read more about [class files and libraries](/editor/Class%20files,%20projects.html).

To add a class file, project or other library to each new script, in **Options > Templates** select **Custom** and edit the template.