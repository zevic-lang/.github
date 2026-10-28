# Contributing to Zevic

Thank you for your interest. Zevic is in an early stage, so the most useful contributions right now are bug reports, small fixes, tests, and feedback on the specification.

## Before you start

- Search existing issues and pull requests first.
- For anything larger than a small fix, open an issue to discuss it before writing code.
- By contributing, you agree that your contribution is licensed under the license of the repository (Apache-2.0 for the compiler, tools, and standard library).

## Changing the language

The language is defined by the specification in the `docs` repository. Changes to the language (syntax, types, standard library API) go through a proposal:

1. Copy `proposals/0000-template.md` to `proposals/NNNN-short-title.md`.
2. Describe the motivation, the design, alternatives, and the cost of the change.
3. Open a pull request. Discussion happens on the pull request.
4. Once accepted, update the specification in the same or a follow-up pull request.

The design values are: simple over powerful, explicit over implicit, and one obvious way to write things.

## Pull requests

- Branch from `main`. Do not push directly to `main`.
- Keep each pull request focused on one change.
- Add or update tests. Compiler changes need a golden test (`.zev` file plus expected output) under `tests/`.
- Run the build and tests locally before opening the pull request.
- Run `zevfmt -check` on any `.zev` files you touch (once `zevfmt` is available).
- CI runs on Linux, macOS, and Windows and must pass.

## Commit messages

- Written in English.
- The first line is a short summary in the imperative mood (`Add overflow check for I32 addition`), up to about 72 characters.
- Add a body that explains why, when the reason is not obvious.

## Code style

- Compiler and runtime (C): C11, 4-space indentation, no compiler warnings with `-Wall -Wextra`.
- Zevic code: formatted by `zevfmt`. There are no style options.

## Reporting bugs

Use the bug report issue template. Include the Zevic version, the platform, a minimal program that reproduces the problem, and the actual and expected output.

## Security issues

Do not open a public issue. See [SECURITY.md](SECURITY.md).

## Code of conduct

All participation is covered by the [Code of Conduct](CODE_OF_CONDUCT.md).
