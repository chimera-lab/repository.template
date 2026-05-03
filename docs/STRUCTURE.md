# :file_folder: Repository Structure

## :book: Table of Contents

- [:file_folder: Repository Structure](./#file_folder-repository-structure)
  - [:telescope: Overview](./#telescope-overview)
  - [:building_construction: Structure](./#building_construction-structure)
    - [:building_construction: Layer Separation Rules](./#building_construction-layer-separation-rules)
      - [:building_construction: Semantic Header Vocabulary](./#building_construction-semantic-header-vocabulary)
      - [:building_construction: GitHub Automation Structure](./#building_construction-github-automation-structure)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Structure.Overview"> -->

`directive: <llm prompt="Structure.Overview">`

<!-- </llm> -->

## :building_construction: Structure

<!-- <llm prompt="Structure.Structure"> -->

`directive: <llm prompt="Structure.Structure">`

<!-- </llm> -->

<!-- <llm prompt="Namespace.Section"> -->

`directive: <llm prompt="Namespace.Section">`

<!-- </llm> -->

<!-- <cmr cmd="docs.mappings.list" applied> -->

| Key | Prompt |
| --- | --- |
| `Architecture.Components` | list and describe the main system components, modules, and their responsibilities within this repository |
| `Architecture.Overview` | write a concise technical architecture overview describing the system boundaries, layers, and design goals for this repository |
| `Architecture.Structure` | describe the architectural layers, main directories, integration points, and responsibilities of each part of this repository |
| `Architecture.Technologies` | list and describe the key technologies, frameworks, runtimes, and tooling used in this repository |
| `Installation` | describe how to install or set up this repository for the first time |
| `Organization.Overview` | describe how this repository is organized, including repository type, template inheritance, and ownership context |
| `Overview` | write a concise overview of this repository describing its purpose, scope, and role within the organization |
| `Requirements` | list the prerequisites and requirements needed to use or develop this repository |
| `Roadmap.Overview` | summarize the roadmap, delivery phases, and release progression planned for this repository |
| `Roadmap.ToDoList` | infer to-do list items from the roadmap description, including key milestones, deliverables, and timelines for this repository. you can use `gh` cli |
| `Structure.GitHubAutomation` | document the .github/ directory structure reserved for GitHub automation only, listing the directories and the constraint that all agents/prompts/skills reference documentation via knowledge, never vice versa |
| `Structure.LayerSeparation` | document the layer separation rules for documentation organization, including the hierarchy diagram, the allowed references table between prompts/agents/skills/knowledge/docs layers, and the forbidden references table. mention that the layer graph can be visualized with `cmr graph agents relation` (PlantUML diagram of prompts → agents → skills → knowledge → docs) and `cmr graph docs structure` (documentation file tree) |
| `Structure.Overview` | describe the repository structure, key directories, and how documentation, automation, and implementation files are organized |
| `Structure.References` | list the reference links to related documentation files for this repository structure page |
| `Structure.SemanticHeaders` | describe the standardized semantic header vocabulary used across documentation |
| `Usage` | describe the primary usage patterns and commands for this repository |

<!-- </cmr> -->

<!-- <cmr cmd="docs.directives.list" applied> -->

| Command | Description | Allowed Types |
| --- | --- | --- |
| `app.tech-stack` | Technology stack inferred from project files | `.app`, `.package`, `.scaffold` |
| `docs.directives.list` | List all registered CMR directive handlers with group, command, description, and allowed types | _any_ |
| `docs.headers.list-typed` | List typed (canonical) markdown headers with emoji, category, description and examples | _any_ |
| `docs.mappings.list` | List all LLM header prompt mappings from .chimera-lab/config.json | _any_ |
| `graph.agents-relation` | Agents relation diagram from docs/diagrams/ | `.org`, `.app`, `.package`, `.scaffold`, `.project`, `.topic` |
| `org.activity` | Recent commit activity across the organization | _any_ |
| `org.contributors` | Top contributors across all repositories | _any_ |
| `org.inheritance` | Show template inheritance tree as a mermaid graph | `.org` |
| `org.list` | List all repositories in a table | `.org` |
| `org.pinned` | Pinned repositories in the GitHub organization | `.org` |
| `org.popular` | Top repositories by star count | `.org` |
| `org.recent` | Most recently updated repositories | `.org` |
| `org.releases` | Most recent releases in the organization | _any_ |
| `org.stats` | Show organization-wide repository statistics | `.org` |
| `org.submodules` | List all git submodules in a table | `.org` |
| `org.tools` | List of apps and packages available in the organization | `.org` |
| `org.topic` | List topic repositories as a hierarchical bullet list. Params: depth (max nesting level), path (root dir, default "."). | `.org` |
| `org.types` | Show all repo-type suffixes and their purposes | `.org` |
| `project.list` | List all project repositories in a table | `.org`, `.project` |
| `project.members` | Member repositories in this project, optionally grouped by type | `.project` |
| `project.status` | Health summary for this project (member count, types) | `.project` |
| `project.tree` | Show project structure as a tree | `.org`, `.project` |
| `topic.children` | Tree of child topics and repositories under this topic | `.topic` |
| `topic.index` | Navigable index of all topic repositories | `.topic`, `.org` |

<!-- </cmr> -->

### :building_construction: Layer Separation Rules

<!-- <llm prompt="Structure.LayerSeparation"> -->

`directive: <llm prompt="Structure.LayerSeparation">`

<!-- </llm> -->

#### :building_construction: Semantic Header Vocabulary

<!-- <llm prompt="Structure.SemanticHeaders"> -->

`directive: <llm prompt="Structure.SemanticHeaders">`

<!-- </llm> -->

<!-- <table Emoji="headers.items.*.emoji" Name="headers.items.*.name" Category="headers.items.*.category" Description="headers.items.*.description" Examples="headers.items.*.examples" applied> -->
<!-- <data name="headers"> -->
<!-- <cmr cmd="docs.headers.list-typed" applied> --><!-- </cmr> -->
<!-- </data> -->

| Emoji | Name | Category | Description | Examples |
| --- | --- | --- | --- | --- |
| `:paperclip:` | Appendix | Reference | Supplementary material | Appendix A, Appendix: Glossary |
| `:book:` | Chapter | Navigation | Major document section | Chapter 1: Introduction, Chapter 2: Setup |
| `:hammer_and_wrench:` | Common Problems | Remediation | Known issues and solutions | Common Problems, Troubleshooting |
| `:jigsaw:` | Components | Structure | System components description | Components, Subsystems |
| `:wrench:` | Configuration | Configuration | Configuration options and settings | Configuration, Settings |
| `:busts_in_silhouette:` | Contributing | Community | Contribution guidelines | Contributing |
| `:medal_sports:` | Credits | Community | Contributors and acknowledgments | Credits, Acknowledgments |
| `:control_knobs:` | Customization | Configuration | Customization options | Customization |
| `:page_facing_up:` | Files | Structure | File listings and descriptions | Files, File Layout |
| `:world_map:` | Guides | Navigation | Step-by-step guides and tutorials | Guides, Tutorials |
| `:inbox_tray:` | Installation | Input | Installation instructions | Installation, Setup |
| `:loudspeaker:` | Introduction | Discovery | Introductory content | Introduction, Preface |
| `:scroll:` | License | Legal | License information | License |
| `:package:` | Material | Structure | Materials and resources | Material, Bill of Materials |
| `:notebook:` | Notes | Documentation | Additional notes and remarks | Notes, Remarks |
| `:telescope:` | Overview | Discovery | High-level overview | Overview, Summary |
| `:books:` | References | Reference | External references and links | References |
| `:clipboard:` | Requirements | Specification | Prerequisites and requirements | Requirements, Prerequisites |
| `:link:` | See Also | Reference | Related topics and cross-references | See Also |
| `:dart:` | Skills | Skills | Agent skills and capabilities | Skills, Capabilities |
| `:gear:` | Software | Technology | Software dependencies | Software, Dependencies |
| `:newspaper:` | Sources | Reference | Source materials and citations | Sources, Citations |
| `:compass:` | Step | Navigation | Individual step in guide/chapter | Step 1: Install, Step 2: Configure |
| `:building_construction:` | Structure | Architecture | Structural information | Structure, Architecture |
| `:card_file_box:` | Submodule | Structure | Git submodule information | Submodule, Submodules |
| `:book:` | Table Of Contents | Navigation | Document navigation section | Table Of Contents, TOC |
| `:triangular_ruler:` | Technologies | Technology | Technologies used | Technologies, Tech Stack |
| `:mag:` | Terminology | Reference | Terms and definitions | Terminology, Glossary |
| `:memo:` | To-Do List | Plan | Planned tasks and future work | To-Do List, Backlog |
| `:toolbox:` | Tools | Tools | Tools and utilities | Tools, CLI |
| `:keyboard:` | Usage | Execution | Usage instructions and examples | Usage, Examples |
| `:warning:` | Warnings | Alert | Important warnings and cautions | Warnings, Cautions |

<!-- </table> -->

#### :building_construction: GitHub Automation Structure

<!-- <llm prompt="Structure.GitHubAutomation"> -->

`directive: <llm prompt="Structure.GitHubAutomation">`

<!-- </llm> -->

## :books: References

<!-- <llm prompt="Structure.References"> -->

`directive: <llm prompt="Structure.References">`

<!-- </llm> -->
