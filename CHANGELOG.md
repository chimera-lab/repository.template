# :file_folder: Changelog

## :book: Table of Contents

- [:file_folder: Changelog](./#file_folder-changelog)
  - [:notebook: Notes](./#notebook-notes)
    - [:notebook: v1.0.0 – Public Release](./#notebook-v100-public-release)
    - [:notebook: v0.0.1 – <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> -->](./#notebook-v001-var-keyorgname-applied-chimera-laborg-var)
    - [:notebook: v0.0.2 – AI Usage](./#notebook-v002-ai-usage)

## :notebook: Notes

### :notebook: v1.0.0 – Public Release

Initial public release of `repository.template` — the Tier 0 baseline for all chimera-lab.org repositories.

**Changes**:

- Full CMR compliance: `cmr docs check --strict` passes with 0 errors across all files.
- Created `TEMPLATE.md` documenting template purpose and installation instructions.
- Added `TEMPLATE.md` reference link to `README.md` hero section.
- Applied `<llm applied>` directive coverage to \~95% of prose in all LLM-first files: `README.md`, `DEVELOPMENT.md`, `docs/ARCHITECTURE.md`, `docs/ORGANIZATION.md`, `docs/ROADMAP.md`, `docs/STRUCTURE.md`.
- Standardized variable key from `repository.name` to `repo.name` across all templates.
- Implemented `docs.headers.list-typed` CMR handler exposing full typed-header registry metadata (emoji, name, category, description, examples).
- Enhanced `cmr docs headers list-typed` CLI output with category and examples columns.
- Layout directive in `docs/STRUCTURE.md`: semantic header vocabulary table generated from CMR registry via `<table>` + `<data>` + `<cmr cmd="docs.headers.list-typed">`.
- Fixed `layout-directive-resolver.ts`: `<data>` children are now preserved after render so directives remain idempotent across repeated `cmr docs render --overwrite` calls.
- Fixed `docs.ts` render pipeline: inner `<cmr>` nodes inside layout (`<table>`/`<list>`) ranges are skipped by the flat CMR pass to prevent double-rendering.
- TOC regenerated in all modified files.

### :notebook: v0.0.1 – <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> -->

All repositories adhere to the architectural principles and standards defined by the <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> --> organization.

These guidelines govern system architecture, structural conventions, and quality practices, serving as the baseline for all projects under this organization.

Visit [:globe_with_meridians: <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> -->](https://www.chimera-lab.com/)

### :notebook: v0.0.2 – AI Usage

AI may be used for non-critical tasks (documentation, wording, abstract planning) and, when appropriate, to generate initial code scaffolding.

Any AI-generated output is treated strictly as a starting point and is always carefully reviewed, modified, and validated by a human to enhance development productivity.

System design, architecture, core logic, and final implementation decisions remain fully human-driven.
