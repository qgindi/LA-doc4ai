# File properties | other

## `noWarnings`

Don't show these warnings. Example: `151,3001,CS1234`.

See also [#pragma warning](🔗).

## `testInternal`

Can use internal symbols of these assemblies, like with `InternalsVisibleToAttribute`.
Example:`Assembly1,Assembly2`.

## `postBuild`

A script to run after successfully compiling and creating output files.

Everything is like with `preBuild`.

## `console`

Let the program run with console.

## `xmlDoc`

Create XML documentation file from `///` comments. And print errors in `///` comments when compiling.

XML documentation files are used by code editors to display class/function/parameter info. Also can be used to create HTML documentation.

## `miscFlags`

Miscellaneous flags. May be set by some controls of the **Properties** window.

- 1 - don't add XAML icons from code strings like `"*name color"` to exe resources.
