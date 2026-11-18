# Contributing to Zevic

Thank you for your interest. Zevic is still in development (0.x), so the most useful contributions right now are bug reports, small fixes, tests, examples, and feedback on the specification.

## Before you start

- Search existing issues and pull requests first.
- For anything larger than a small fix, open an issue to discuss it before writing code.
- By contributing, you agree that your contribution is licensed under the license of the repository (Apache-2.0 for the compiler, tools, and standard library).
- You need `make` and clang 15 or newer. No C compiler is needed to build: `make` builds `zevic`, `zevpm` and `zevfmt` from the committed LLVM IR.

## Changing the language

The language is defined by the specification in the `zevic` repository (`docs/spec/zevic-spec.md`). Changes to the language (syntax, types, standard library API) go through a proposal:

1. Copy `docs/proposals/0000-template.md` to `docs/proposals/NNNN-short-title.md` in the `zevic` repository.
2. Describe the motivation, the design, alternatives, and the cost of the change.
3. Open a pull request. Discussion happens on the pull request.
4. Once accepted, update the specification in the same or a follow-up pull request. If the compiler and the specification disagree, fix one of them in the same change.

Existing proposals in `docs/proposals/` show the expected level of detail.

The design values are: simple over powerful, explicit over implicit, and one obvious way to write things.

## Pull requests

- Branch from `main`. Do not push directly to `main`.
- Keep each pull request focused on one change, and keep commits small: one change, one commit.
- Add or update tests. Compiler changes need a golden test: a directory under `tests/golden/` with `input.zev` and either `expected_output.txt` (the program runs) or `expected_error.txt` (compile error).
- Add an entry to the `Unreleased` section of `CHANGELOG.md` in the same commit as the change.
- Run `make` and `make test` locally before opening the pull request.
- Run `zevfmt -check` on any `.zev` files you touch.
- CI runs on Linux, macOS, and Windows and must pass.

## Commit messages

- Written in English.
- The first line is a short summary in the imperative mood (`Add overflow check for I32 addition`), up to about 72 characters.
- Add a body that explains why, when the reason is not obvious.

## Code style

- Zevic code (the compiler `zevic1`, `zevpm`, `zevfmt` and the standard library): formatted by `zevfmt`. There are no style options.
- Runtime and test runner (C): C11, 4-space indentation, no compiler warnings with `-Wall -Wextra`.

## Reporting bugs

Use the bug report issue template in the repository where the problem is (usually `zevic`). Include the Zevic version, the platform, a minimal program that reproduces the problem, and the actual and expected output.

## Security issues

Do not open a public issue. See [SECURITY.md](SECURITY.md).

## Code of conduct

All participation is covered by the [Code of Conduct](CODE_OF_CONDUCT.md).
