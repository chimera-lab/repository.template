# :file_folder: <!-- <var key="repo.name" applied> -->repository.template<!-- </var> -->

<!-- <badges name="brand,license,last-commit,issues,stars" applied> -->

[![chimera-lab build · share · evolve](https://img.shields.io/badge/chimera--lab-build_·_share_·_evolve-6e40c9?style=flat-square)](https://github.com/chimera-lab)
[![License](https://img.shields.io/github/license/chimera-lab/repository.template?style=flat-square)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/commits)
[![Issues](https://img.shields.io/github/issues/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/issues)
[![Stars](https://img.shields.io/github/stars/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/stargazers)

<!-- </badges> -->

## :book: Table of Contents

- [:file_folder: <!-- <var key="repo.name" applied> -->repository.template<!-- </var> -->](./#file_folder-var-keyreponame-applied-repositorytemplate-var)
  - [:telescope: Overview](./#telescope-overview)
  - [:clipboard: Requirements](./#clipboard-requirements)
  - [:inbox_tray: Installation](./#inbox_tray-installation)
  - [:keyboard: Usage](./#keyboard-usage)
  - [:books: References](./#books-references)

## :telescope: Overview

<!-- <llm prompt="Overview" applied> -->

This repository provides the baseline documentation and workflow template for a software project in the <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> --> ecosystem. It defines a consistent structure for repository guidance, agent-driven collaboration, reusable skills, and supporting knowledge so teams can implement, maintain, review, and document work with the same patterns across projects.

<!-- </llm> -->

<!-- <cmr cmd="repo.tags[name=repository.template]"> -->

`directive: <cmr cmd="repo.tags[name=repository.template]">`

<!-- </cmr> -->

## :clipboard: Requirements

<!-- <llm prompt="Requirements" applied> -->

- Git installed locally and access to a GitHub repository with permission to create branches, commits, and pull requests.
- A standard development environment on Linux, macOS, or Windows; a Bash-compatible shell is recommended for command-line workflows.
- A text editor or IDE that can edit Markdown, YAML, and source files used by the repository.
- Working knowledge of basic Git operations, pull request review, and repository-based collaboration.
- If repository automation is used, access to the relevant GitHub Actions, secrets, and environment configuration is required.

Keep local tooling aligned with the versions and conventions defined by the repository itself.

<!-- </llm> -->

## :inbox_tray: Installation

<!-- <llm prompt="Installation" applied> -->

This repository is intended to be used as a GitHub template rather than installed as a package.

1. Create a new repository from this template using **Use this template** on GitHub.
2. Clone your new repository locally:
   ```bash
   git clone <your-repository-url>
   cd <your-repository-name>
   ```
3. Review the template files, replace placeholder content, and commit your project-specific changes.

If you are evaluating the template before creating a repository, you can clone it directly and inspect the structure locally.

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Usage" applied> -->

Use this repository as the starting point for a new Chimera-compatible project.

1. Create a new repository from this template.
2. Replace template variables, placeholders, and organization-specific values.
3. Update the agent, prompt, skill, knowledge, and documentation files for your project.
4. Keep the intended structure intact: prompts -> agent manager -> subagents -> skills -> knowledge -> docs.
5. Review repository automation and validation files before publishing.

After setup, use the repository as the canonical source for your agent architecture, documentation structure, and collaboration conventions.

<!-- </llm> -->

## :books: References

- [:page_facing_up: CODE\_OF\_CONDUCT.md](CODE_OF_CONDUCT.md)
- [:page_facing_up: CONTRIBUTING.md](CONTRIBUTING.md)
- [:page_facing_up: SECURITY.md](SECURITY.md)
- [:page_facing_up: ./docs/STRUCTURE.md](./docs/STRUCTURE.md) - Project Structure
- [:page_facing_up: ./docs/ORGANIZATION.md](./docs/ORGANIZATION.md) - Managing entity
