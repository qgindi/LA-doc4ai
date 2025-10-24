# Code editor - Rename symbol

The **Rename symbol** command finds symbol definition/references like the **Find references** command, and replaces all with the specified new name. It is similar to the "Find and replace text in files" feature, but more precise.

If checked **Include comments/disabled/strings** and finds the word in comments/disabled/strings, at first displays these results in the **Found** panel. You can right-click some of them to exclude. Finally click the **Replace** link. The same if finds symbol usages that are ambiguous or error, for example a method name without parameters used in documentation comments `cref`.

It also automatically resolves name conflicts where possible, for example prepends namespace name.