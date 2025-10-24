# File properties - `com` (buttons **COM** and **...**)

Use a COM interop assembly. Meta comment `/*/ com File.dll; /*/`.

In the **Properties** window select a COM component. It immediately converts the type library to a COM interop assembly and saves the assembly file in `%folders.Workspace%\.interop`.

An interop assembly is a .NET assembly without real code. Not used at run time. At run time is used the COM component (registered unmanaged dll or exe file). If a COM dll for current platform unavailable, try to set role `exeProgram` and change platform.

To remove this meta comment, edit the code. Optionally delete unused interop assemblies.
 To use `extern alias Abc;`, edit the code: `/*/ com File.dll /alias=Abc; /*/`