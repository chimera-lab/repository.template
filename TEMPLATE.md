# :package: repository.template

This repository **is a template**, not a project. It is the universal baseline for all `chimera-lab` repositories: every other repository in the organization (apps, packages, scaffolds, projects, topics, etc.) inherits from it directly or transitively.

If you reached this page from GitHub looking for a project to use, you probably want one of the downstream repositories instead. If you want to **start a new repository based on this template**, read on.

## :book: Table of Contents

- [:package: repository.template](./#package-repositorytemplate)
  - [:telescope: Overview](./#telescope-overview)
  - [:inbox_tray: Installation](./#inbox_tray-installation)
  - [:building_construction: Structure](./#building_construction-structure)
  - [:books: References](./#books-references)

## :telescope: Overview

A complete, opinionated repository skeleton with:

- Root governance files: `LICENSE`, `CHANGELOG.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `AGENTS.md`, `DEVELOPMENT.md`, `Makefile`.
- A `docs/` baseline (`ARCHITECTURE.md`, `STRUCTURE.md`, `ORGANIZATION.md`, `ROADMAP.md`, `diagrams/`, `knowledge/`).
- A `.github/` baseline (`ISSUE_TEMPLATE/`, `agents/`, `prompts/`, `skills/`, `workflows/`).
- Repository tooling: `.editorconfig`, `.gitattributes`, `.gitignore`, `.pre-commit-config.yaml`.
- A directive system (`<var>`, `<llm>`, `<cmr>`, `<fragment>`, `<i18n>`, layout) that the `cmr` CLI uses to render and validate documentation consistently across all derived repositories.

## :inbox_tray: Installation

```bash
cmr repo init --template repository.template <new-repo-name>
```

This produces a new repository pre-wired to inherit from this baseline. Updates published here can later be propagated to your repository with:

```bash
cmr repo template upgrade
```

## :building_construction: Structure

What downstream consumers inherit from this template:

- **LLM-first documents** (per-repo content, baseline ships placeholders): `README.md`, `docs/ARCHITECTURE.md`, `docs/STRUCTURE.md`, `docs/ORGANIZATION.md`, `docs/ROADMAP.md`, `DEVELOPMENT.md`.
- **Authored documents** (governance, inherited verbatim): `AGENTS.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `LICENSE`.
- **Mandatory directories**: `docs/` (full set) and `.github/` (full set).

## :books: References

- [:page_facing_up: README.md](README.md) - The README this template ships to downstream repositories (contains pending directives by design).
- [:page_facing_up: AGENTS.md](AGENTS.md) - Agent orchestration model used across the organization.
- [:page_facing_up: CONTRIBUTING.md](CONTRIBUTING.md) - How to contribute to this template itself.
- [:page_facing_up: docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) - Architectural overview.
- [:page_facing_up: docs/STRUCTURE.md](docs/STRUCTURE.md) - File and directory layout.
