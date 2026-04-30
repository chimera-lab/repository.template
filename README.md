# :file_folder: <!-- <var key="repo.name" applied> -->repository.template<!-- </var> -->

<!-- <badges name="brand" applied> -->

[![chimera-lab build · share · evolve](https://img.shields.io/badge/chimera--lab-build_·_share_·_evolve-6e40c9?style=flat-square)](https://github.com/chimera-lab)

<!-- </badges> -->

<!-- <badges name="license,last-commit,issues,stars" layout="inline" applied> -->

[![License](https://img.shields.io/github/license/chimera-lab/repository.template?style=flat-square)](LICENSE) [![Last commit](https://img.shields.io/github/last-commit/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/commits) [![Issues](https://img.shields.io/github/issues/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/issues) [![Stars](https://img.shields.io/github/stars/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/stargazers)

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

This repository provides the standard foundation for software projects in the <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> --> ecosystem. It defines a consistent starting point for repository structure, documentation, agent configuration, prompts, and supporting conventions so projects can be created and maintained with the same operational model.

Use this template to bootstrap or align repositories that need predictable organization, maintainable documentation, and compatibility with the broader Chimera workflow. It is intended to reduce setup effort, improve consistency across projects, and make collaboration easier for both humans and automation.

<!-- </llm> -->

<!-- <cmr cmd="repo.tags[name=repository.template]"> -->

`directive: <cmr cmd="repo.tags[name=repository.template]">`

<!-- </cmr> -->

## :clipboard: Requirements

<!-- <llm prompt="Requirements" applied> -->

- A GitHub repository with permission to manage repository content and the `.github/` configuration tree.
- Standard Git tooling for local editing, review, and synchronization.
- A Markdown-based documentation workflow that preserves the template structure and internal references.
- The Chimera agent layout in `.github/agents/`, `.github/prompts/`, and related skills/knowledge files when using the repository’s agent-driven workflows.
- GitHub Actions support if repository automation, validation, or publishing workflows are enabled.

<!-- </llm> -->

## :inbox_tray: Installation

<!-- <llm prompt="Installation" applied> -->

This repository is a template. Create a new repository from it first, then clone your generated project locally:

```bash
git clone <your-repository-url>
cd <your-repository-directory>
```

Install dependencies with the package manager used by your project, for example:

```bash
# JavaScript / TypeScript
npm install

# Python
pip install -r requirements.txt

# Go
go mod tidy
```

If the project includes environment configuration, copy the example file and update it for your local setup before running the application. Refer to the repository's `package.json`, language manifest, or project-specific guides for the exact commands used by your implementation.

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Usage" applied> -->

1. Create a new repository from this template.

2. Replace the template placeholders with values for your project or organization, especially the `<!-- <var ...> -->` variables used across the documentation.

3. Update the core repository metadata and guidance:
   - `README.md`
   - `.github/agents/`
   - `.github/prompts/`
   - `.github/skills/`
   - `.github/copilot-instructions.md`

4. Remove sections, prompts, skills, or knowledge files that do not apply to your workflow, and add any project-specific conventions your agents should follow.

5. Review the generated documentation structure to ensure links, references, and header hierarchy match your intended repository layout.

6. Commit the customized template as the baseline for your project before adding feature-specific content.

<!-- </llm> -->

## :books: References

- [:page_facing_up: CODE\_OF\_CONDUCT.md](CODE_OF_CONDUCT.md)
- [:page_facing_up: CONTRIBUTING.md](CONTRIBUTING.md)
- [:page_facing_up: SECURITY.md](SECURITY.md)
- [:page_facing_up: ./docs/STRUCTURE.md](./docs/STRUCTURE.md) - Project Structure
- [:page_facing_up: ./docs/ORGANIZATION.md](./docs/ORGANIZATION.md) - Managing entity
