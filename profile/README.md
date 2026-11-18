<p align="center">
  <img src="https://zevic-lang.github.io/assets/img/logo.png" alt="Zevic" width="160">
</p>

# Zevic

A small native language that uses C code as it is. Zevic turns source code into LLVM IR and lets clang build and link it. The compiler is written in Zevic itself.

**Website: [zevic-lang.github.io](https://zevic-lang.github.io)** ([日本語](https://zevic-lang.github.io/) / [English](https://zevic-lang.github.io/en/))

```zevic
module Main

import Zevic.Console

fn Main() {
    Console.Println("Hello, World!")
}
```

```sh
zevic hello.zev -o hello && ./hello
```

- **Easy to write**: explicit types, no implicit conversions, no null, no exceptions (`Option` / `Result` and `?`).
- **C interop built in**: call C with `extern "C"`, expose functions with `export "C"`, and build C sources together with Zevic.
- **Garbage collected**: the Boehm GC is bundled.
- **Self-hosted**: `zevic1` is written in Zevic and rebuilds itself to byte-identical LLVM IR.
- **Batteries included**: `zevic` (compiler), `zevpm` (package manager), `zevfmt` (formatter), `test` blocks, and a standard library of 30+ modules.

> Status: version 0.4.x. It works, but it is still in development, so the language and the library API may change before 1.0.

## Install

See [Install](https://zevic-lang.github.io/en/install/) for Ubuntu / Debian (apt), Windows (winget), macOS, Linux archives and Termux.

## Repositories

| Repository | What it contains |
| --- | --- |
| [`zevic`](https://github.com/zevic-lang/zevic) | Compiler, `zevpm`, `zevfmt`, runtime, standard library, language specification, proposals |
| [`examples`](https://github.com/zevic-lang/examples) | Sample programs with their expected output |
| [`zevic-lang.github.io`](https://github.com/zevic-lang/zevic-lang.github.io) | The website (Jekyll) |
| [`zevic-c`](https://github.com/zevic-lang/zevic-c) | The first compiler, written in C (archived) |

## Get involved

Bug reports, small fixes, tests, examples and feedback on the specification are all welcome. Read [CONTRIBUTING.md](https://github.com/zevic-lang/.github/blob/main/CONTRIBUTING.md) first. Language changes go through [proposals](https://github.com/zevic-lang/zevic/tree/main/docs/proposals).

---

Zevic は、C のコードをそのまま使える、小さくて書きやすいネイティブ言語です。詳しくは[公式サイト](https://zevic-lang.github.io/)をご覧ください。
