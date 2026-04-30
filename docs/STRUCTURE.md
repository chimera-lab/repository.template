# :file_folder: Repository Structure

## :book: Table of Contents

- [:file_folder: Repository Structure](./#file_folder-repository-structure)
  - [:telescope: Overview](./#telescope-overview)
  - [:building_construction: Structure](./#building_construction-structure)
    - [:building_construction: CMR Directive Catalog](./#building_construction-cmr-directive-catalog)
    - [:building_construction: Layer Separation Rules](./#building_construction-layer-separation-rules)
    - [:building_construction: Semantic Header Vocabulary](./#building_construction-semantic-header-vocabulary)
    - [:building_construction: GitHub Automation Structure](./#building_construction-github-automation-structure)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Structure.Overview" > -->

This repository is organized as a documentation-first template for maintaining consistent project standards. The root directory contains the primary repository documents and operational references, including the main overview, template guidance, contribution and development policies, security and conduct documents, licensing, and release history. Supporting material lives under `docs/`, where deeper references and visual artifacts can be kept without cluttering the top level.

The structure is intentionally simple: core documents stay easy to find, while supplementary guidance is separated into dedicated documentation space. This keeps the repository readable for contributors, predictable for automation, and easy to reuse as a standardized foundation for new projects.

<!-- </llm> -->

## :building_construction: Structure

<!-- <llm prompt="Structure.Structure"> -->

`directive: <llm prompt="Structure.Structure">` for README sections such as `Overview` or `Usage`

`directive: <llm prompt="Namespace.Section">` for documentation pages such as `Architecture.Overview`

**Active mappings by file**:

```text
README.md:
  llm<Overview>
  llm<Requirements>
  llm<Installation>
  llm<Usage>

STRUCTURE.md:
  llm<Structure.Overview>

ORGANIZATION.md:
  llm<Organization.Overview>

ROADMAP.md:
  llm<Roadmap.Overview>

ARCHITECTURE.md:
  llm<Architecture.Overview>
  llm<Architecture.Structure>
  llm<Architecture.Technologies>
```

**Validation**: Run `cmr docs check --tags` to validate all render directives map to active header prompts.

**Resolution policy**:

- Default location: repository `.chimera-lab/settings.json` under `llm.headerPrompts`
- Optional shared location: organization-level settings when the same prompt set is reused across multiple templates or repositories
- Override rule: keep repository-specific overrides minimal and only for genuinely divergent wording or structure

<!-- </llm> -->

#### :building_construction: CMR Directive Catalog

<!-- <llm prompt="Structure.DirectiveCatalog"> -->

CMR directives are reserved for generated repository and organization inventories. They should be used only when the content is expected to be refreshed by `cmr docs render`.

**Syntax**:

```html
<!-- <cmr cmd="group.command[key=value,...]"> -->

`directive: <cmr cmd="group.command[key=value,...]">`

<!-- </cmr> -->
<!-- <cmr cmd="group.command"> -->

`directive: <cmr cmd="group.command">`

<!-- </cmr> -->
```

**Supported baseline directives in current workspace**:

```text
project.list
org.list
org.list[suffix=app]
org.list[suffix=scaffold]
org.topic
org.submodules
org.types
org.inheritance
org.stats
```

**Usage by repository type**:

- `topic.template`: prefer `org.submodules` in README-level overview pages listing contained subrepositories.
- `project.template`: prefer `project.list` when a repository acts as an aggregate of project entries.
- `org.template`: allow `org.list[...]`, `org.topic`, `org.types`, `org.inheritance`, and `org.stats` for organization-wide inventories.
- `app.template`, `package.template`, `scaffold.template`: avoid CMR directives by default unless the repository is explicitly acting as an index or generated registry.

**Rules**:

- Use LLM directives for narrative content.
- Use CMR directives only for generated tables, lists, or aggregate inventories.
- Do not invent new directives in templates without first verifying resolver support in CMR knowledge and implementation.
- Preserve `;applied` only for rendered output; source templates should keep the unresolved directive form.

<!-- </llm> -->

#### :building_construction: Layer Separation Rules

<!-- <llm prompt="Structure.LayerSeparation"> -->

Documentation organization follows strict layer boundaries to maintain clarity and reusability:

```text
prompts (frontmatter: agent, skills)
├── agents (`:dart: Skills` section)
├── skills (`:books: References` to knowledge)
├── knowledge (`:books: References` to docs)
└── docs (`:books: References` to external)
```

**Allowed references**:

| From      | To                | Via                              | Allowed |
| --------- | ----------------- | -------------------------------- | ------- |
| Knowledge | docs/             | `:books: References`             | ✅ YES   |
| Knowledge | sibling knowledge | `:books: References`             | ✅ YES   |
| Skill     | Knowledge         | `:books: References` in SKILL.md | ✅ YES   |
| Agent     | Skill             | `:dart: Skills` section          | ✅ YES   |
| Prompt    | Agent             | Frontmatter `agent:`             | ✅ YES   |
| Prompt    | Skill             | Content references               | ✅ YES   |

**Forbidden references**:

| From      | To        | Reason                 |
| --------- | --------- | ---------------------- |
| Agent     | Agent     | No horizontal coupling |
| Skill     | Skill     | No horizontal coupling |
| Prompt    | Prompt    | No horizontal coupling |
| Knowledge | Agent     | Breaks layer boundary  |
| Docs      | Knowledge | One-way flow only      |

<!-- </llm> -->

#### :building_construction: Semantic Header Vocabulary

<!-- <llm prompt="Structure.SemanticHeaders"> -->

All headers must use emoji prefixes from the standardized vocabulary. The table below is generated from the canonical typed-header registry exposed by `cmr docs headers list-typed`:

<!-- <table Emoji="headers.items.*.emoji" Name="headers.items.*.name" Category="headers.items.*.category" Description="headers.items.*.description" Examples="headers.items.*.examples" applied> -->

<!-- <data name="headers"> -->

<!-- <cmr cmd="docs.headers.list-typed"> -->

`directive: <cmr cmd="docs.headers.list-typed">`

<!-- </cmr> -->

<!-- </data> -->

| Emoji                     | Name              | Category      | Description                         | Examples                                  |
| ------------------------- | ----------------- | ------------- | ----------------------------------- | ----------------------------------------- |
| `:paperclip:`             | Appendix          | Reference     | Supplementary material              | Appendix A, Appendix: Glossary            |
| `:book:`                  | Chapter           | Navigation    | Major document section              | Chapter 1: Introduction, Chapter 2: Setup |
| `:hammer_and_wrench:`     | Common Problems   | Remediation   | Known issues and solutions          | Common Problems, Troubleshooting          |
| `:jigsaw:`                | Components        | Structure     | System components description       | Components, Subsystems                    |
| `:wrench:`                | Configuration     | Configuration | Configuration options and settings  | Configuration, Settings                   |
| `:busts_in_silhouette:`   | Contributing      | Community     | Contribution guidelines             | Contributing                              |
| `:medal_sports:`          | Credits           | Community     | Contributors and acknowledgments    | Credits, Acknowledgments                  |
| `:control_knobs:`         | Customization     | Configuration | Customization options               | Customization                             |
| `:page_facing_up:`        | Files             | Structure     | File listings and descriptions      | Files, File Layout                        |
| `:world_map:`             | Guides            | Navigation    | Step-by-step guides and tutorials   | Guides, Tutorials                         |
| `:inbox_tray:`            | Installation      | Input         | Installation instructions           | Installation, Setup                       |
| `:loudspeaker:`           | Introduction      | Discovery     | Introductory content                | Introduction, Preface                     |
| `:scroll:`                | License           | Legal         | License information                 | License                                   |
| `:package:`               | Material          | Structure     | Materials and resources             | Material, Bill of Materials               |
| `:notebook:`              | Notes             | Documentation | Additional notes and remarks        | Notes, Remarks                            |
| `:telescope:`             | Overview          | Discovery     | High-level overview                 | Overview, Summary                         |
| `:books:`                 | References        | Reference     | External references and links       | References                                |
| `:clipboard:`             | Requirements      | Specification | Prerequisites and requirements      | Requirements, Prerequisites               |
| `:link:`                  | See Also          | Reference     | Related topics and cross-references | See Also                                  |
| `:dart:`                  | Skills            | Skills        | Agent skills and capabilities       | Skills, Capabilities                      |
| `:gear:`                  | Software          | Technology    | Software dependencies               | Software, Dependencies                    |
| `:newspaper:`             | Sources           | Reference     | Source materials and citations      | Sources, Citations                        |
| `:compass:`               | Step              | Navigation    | Individual step in guide/chapter    | Step 1: Install, Step 2: Configure        |
| `:building_construction:` | Structure         | Architecture  | Structural information              | Structure, Architecture                   |
| `:card_file_box:`         | Submodule         | Structure     | Git submodule information           | Submodule, Submodules                     |
| `:book:`                  | Table Of Contents | Navigation    | Document navigation section         | Table Of Contents, TOC                    |
| `:triangular_ruler:`      | Technologies      | Technology    | Technologies used                   | Technologies, Tech Stack                  |
| `:mag:`                   | Terminology       | Reference     | Terms and definitions               | Terminology, Glossary                     |
| `:memo:`                  | To-Do List        | Plan          | Planned tasks and future work       | To-Do List, Backlog                       |
| `:toolbox:`               | Tools             | Tools         | Tools and utilities                 | Tools, CLI                                |
| `:keyboard:`              | Usage             | Execution     | Usage instructions and examples     | Usage, Examples                           |
| `:warning:`               | Warnings          | Alert         | Important warnings and cautions     | Warnings, Cautions                        |

<!-- </table> -->

<!-- </llm> -->

#### :building_construction: GitHub Automation Structure

<!-- <llm prompt="Structure.GitHubAutomation"> -->

`.github/` reserved for GitHub-specific automation **only**. No documentation content in `.github/docs/` or `.github/`.

**Directories**:

- `agents/`: AI agent definitions (`*.agent.md` with frontmatter)
- `prompts/`: Prompt templates (`*.prompt.md` with frontmatter)
- `skills/`: Agent skills (referenced by agents, not duplicated here)
- `workflows/`: GitHub Actions (`.yml` files)
- `ISSUE_TEMPLATE/`: GitHub issue templates

**Constraint**: All agents/prompts/skills reference documentation via knowledge, never vice versa.

<!-- </llm> -->

## :books: References

<!-- <llm prompt="Structure.References"> -->

- [:page_facing_up: ORGANIZATION.md](ORGANIZATION.md)
- [:page_facing_up: ../../README.md](../../README.md)
- [:page_facing_up: knowledge/validating.knowledge.md](knowledge/validating.knowledge.md)
- [:page_facing_up: knowledge/reviewing.knowledge.md](knowledge/reviewing.knowledge.md)

<!-- </llm> -->
