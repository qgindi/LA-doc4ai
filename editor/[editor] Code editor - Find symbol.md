# Code editor - Find symbol

The **Find symbol** command shows a temporary window to find a symbol by name and go to its definition.

The search query can contain one or several parts of symbol name, like `part1 part2`. Or include the containing type, like `Type.name`. Or like `FM` to find `FindMe`.

To find only types, use prefix `t`, like `t name` or `t:name`. Prefix `m` is for members (function, field), `n` for namespaces.

To select a symbol, click or use arrow/page keys and `Enter`.

Finds symbols defined in current file or project + files and projects included through `/*/ c /*/` and `/*/ pr /*/`.