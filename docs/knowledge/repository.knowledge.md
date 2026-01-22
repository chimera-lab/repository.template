---
name: repository
description: Repository management patterns and workflows
---

# :file_folder: Repository Management Knowledge

## :book: Table of Contents

- [:file\_folder: Repository Management Knowledge](./#file_folder-repository-management-knowledge)
  - [:book: Table of Contents](./#book-table-of-contents)
  - [:telescope: Overview](./#telescope-overview)
  - [:triangular\_ruler: Technologies](./#triangular_ruler-technologies)
    - [:triangular\_ruler: Metadata Files](./#triangular_ruler-metadata-files)
    - [:triangular\_ruler: Documentation Structure](./#triangular_ruler-documentation-structure)
  - [:world\_map: Guides](./#world_map-guides)
    - [:world\_map: Branching Strategy](./#world_map-branching-strategy)
    - [:world\_map: Commit Convention](./#world_map-commit-convention)
  - [:toolbox: Tools](./#toolbox-tools)
  - [:books: References](./#books-references)

## :telescope: Overview

This document describes repository management patterns, workflows, and best practices for chimera-lab repositories.

## :world_map: Guides

### :world_map: Branching Strategy

- `main` - Stable release branch
- `develop` - Active development
- `feature/*` - Feature branches
- `fix/*` - Bug fixes

### :world_map: Conventional Commits

```text
<type>: <description>

feat: add new feature
fix: resolve bug
docs: update documentation
chore: maintenance tasks
refactor: code restructuring
```

## :toolbox: Tools

## :toolbox: `cmr`

The CMR CLI (`cmr`) automates chimera-lab repositories managing documentation validation, milestones, issues, labels, and git operations for submodules and templates. It unifies discovery, GitHub resources, and template workflows.

## :books: References

- [:page_facing_up: ../../DEVELOPMENT.md](../../DEVELOPMENT.md)
- [:page_facing_up: ../../CONTRIBUTING.md](../../CONTRIBUTING.md)
