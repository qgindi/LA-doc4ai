# Code editor - WPF window preview

The program does not have a dialog window editor/designer, but it's easy to create windows in code, using class `Au.wpfBuilder`. The program can automatically show/update the window while you edit its code, if it contains code like this:

```
#if WPF_PREVIEW
b.Window.Preview();
#endif
```

This code must be after building the window but before showing it (`Au.wpfBuilder.ShowDialog` etc).

To activate this feature for current document, check toolbar button **WPF preview** or menu **Edit > View > WPF preview**.

How it works: If **WPF preview** is checked and current script contains `#if WPF_PREVIEW`, the program launches/restarts the script whenever you make changes in its code, unless there are errors. The script runs like when clicked the **Run** button, with these changes:

- Defined `WPF_PREVIEW`. In script you use `#if WPF_PREVIEW` to include preview-specific code. Or use `Au.script.isWpfPreview`.
- Function **Preview** shows the window without activating. Also changes some its properties. Ends the process when the window closed.
- Some `/*/ properties /*/` are ignored: `role`, `ifRunning`, `uac`, `platform`, `console`, `optimize`, `outputPath`, `preBuild`, `postBuild`, `xmlDoc`.
- If current file (or its main project file) is a class file, runs it as a script; ignores the test script. Therefore need `#if WPF_PREVIEW` code that runs at startup and calls the function that contains the window code.
- Function `Au.script.setup` does nothing.

In preview mode the script must go straight to the window code. If normally it doesn't, add code like this somewhere at the start:

```
#if WPF_PREVIEW
FunctionContainingWindowCode();
#endif
```

If it's a dialog class, add code like this:

```
#if WPF_PREVIEW
new DialogClass().Preview();
#endif
```

or this:

```
#if WPF_PREVIEW
class Program { static void Main() { new DialogClass().Preview(); }}
#endif
```

In preview mode the script must not activate or move the window. Should skip slow/expensive operations that aren't necessary for preview. Should not show the tray icon.