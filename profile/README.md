# Zevic

Zevic is a small, friendly, natively compiled language that can use C libraries without glue code.

```
module Main

import Zevic.Console as ZC

fn Main(args: Array<String>) ->Unit {
    ZC.Println("Hello, World!")
}
```

- **Simple**: C#-like syntax, explicit types, no implicit conversions, no null.
- **C interop built in**: call C with `extern "C"`, expose functions with `export "C"`. No header files needed.
- **Garbage collected**: no manual memory management.
- **LLVM backend**: the compiler emits LLVM IR and uses `clang` to build and link.
- **Batteries included**: `zevic` (compiler), `zevpm` (package manager), `zevfmt` (formatter), built-in `test` blocks.

> Status: early design stage. The language specification is a draft.

## Repositories

| Repository | What it contains |
| --- | --- |
| [`zevic`](https://github.com/zevic-lang/zevic) | Compiler and runtime |
| [`docs`](https://github.com/zevic-lang/docs) | Language specification, tutorials, proposals |
| [`examples`](https://github.com/zevic-lang/examples) | Sample programs |

## Get involved

Read [CONTRIBUTING.md](https://github.com/zevic-lang/.github/blob/main/CONTRIBUTING.md) first. Language changes go through proposals in the `docs` repository.
