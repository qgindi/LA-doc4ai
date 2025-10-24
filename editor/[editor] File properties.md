# C# file properties

C# file properties in LibreAutomate are similar to C# project properties in Visual Studio. Most properties are stored in `/*/ meta comments /*/` at the start of code. Can be edited in the **Properties** window or in code.

Meta comments syntax:

- The block of meta comments starts and ends with `/*/`. Only the first such block is used.
- The block of meta comments must be at the start. Can be preceded by comments and empty lines.
- Property name and value are separated by space.
- Multiple properties separated by `;` or/and newlines.
- Property names must match case.
- Property values are not enclosed in quotes etc.
- There are no escape sequences.

Example - single line:

```
/*/ role exeProgram; outputPath %folders.Workspace%\exe\Script1; /*/
```

Example - multiple lines:

```
/*/
role exeProgram
outputPath %folders.Workspace%\exe\Script1
/*/
```

The compilation may contain multiple C# files (files in the project folder and files added using meta comment `c`). Properties are applied to the entire compilation, not only to the file where specified. Most properties can be specified only in the main file of the compilation (error if not); others can be anywhere (`c`, `r`, `pr`, `nuget`, `com`, `resource`, `file`). Most properties can be specified once (error if not); others can be multiple (`c`, `r`, `pr`, `nuget`, `com`, `resource`, `file`, `noRef`). Some properties are available only for some roles.

Terms used this article:

- *property* and *meta comment* are synonyms.
- *editor* and *LibreAutomate* are synonyms.
- *script file* - a C# file that can be executed directly (like a program).
- *class file* - a C# file that contains classes/functions that can be used in other files.
- *project folder* or *project* - folder named like `@Example` (starts with `@`). The first C# file (*main file*) and all class files are automatically added to the compilation.
- *compilation* - one or more C# files that are compiled together to create a program or library.

Properties in this article are grouped like in the **Properties** window.