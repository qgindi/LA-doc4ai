# File properties - `platform`

CPU instruction set.

- `x64` - runs on all modern Windows computers (x64, Windows11+ ARM64).
- `arm64` - runs only on Windows ARM64. Used because x64 and x86 programs are slow there.
- `x86` - runs on almost all Windows computers (x64, x86, all ARM64), as 32-bit process.

Default - as LibreAutomate and the Windows OS on this computer (x64 or arm64).

Creates program files for this platform. If `optimize true` and `platform` not `x86`, creates for both x64 and arm64. In any case, the process uses this platform when launched from editor.

Most .NET dlls can be used by programs of any platform. But native dlls can be used only in programs of the same platform as of the dll. Usually libraries that use native dlls have dll files for multiple platforms. If a dll for some platform is missing, you can't use that platform for your script/program that will use that library. Workaround: use role `exeProgram` and platform of an available dll.