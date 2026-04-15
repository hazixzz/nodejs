# AGENTS.md

Non-discoverable rules for the Node.js codebase.

## Landmines

- `make test-only` must run from the working directory where local changes are applied, not a separate clone.
- `make lint` is comprehensive: JS, C++, Markdown, YAML, doc, addon-doc, and shell scripts.
- CI lint (`lint-ci`) adds Python linting, which requires `make lint-py-build` first.

## Commands

- `make lint` — full local lint check
- `make lint-js-fix` — auto-fix JS lint errors
- `make test-only` — run tests only (no rebuild)
- `make -j4 test` — full check including documentation tests

## Rules

- PRs go to upstream `main`.
- Commit messages use Node.js format: `subsystem: description`

## Discoverable in code/config

- `BUILDING.md` — prerequisites and build instructions
- `CONTRIBUTING.md` — contribution workflow
- `doc/contributing/pull-requests.md` — PR process
- `GOVERNANCE.md` — project governance
- `Makefile` — all build/test/lint targets
