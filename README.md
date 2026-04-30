# :file_folder: <!-- <var key="repo.name" applied> -->repository.template<!-- </var> -->

<!-- <badges name="brand,license,last-commit,issues,stars" applied> -->

[![chimera-lab build · share · evolve](https://img.shields.io/badge/chimera--lab-build_·_share_·_evolve-6e40c9?style=flat-square)](https://github.com/chimera-lab)\
[![License](https://img.shields.io/github/license/chimera-lab/repository.template?style=flat-square)](LICENSE)\
[![Last commit](https://img.shields.io/github/last-commit/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/commits)\
[![Issues](https://img.shields.io/github/issues/chimera-lab/repository.template?style=flat-square)](https://github.com/chimera-lab/repository.template/issues)\
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

This repository provides the standard template for software repositories in <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> -->. It establishes a consistent foundation for project documentation, agent-oriented workflows, reusable prompts and skills, and repository structure so new and existing projects follow the same conventions.

Use this template as the baseline for creating or aligning repositories that need clear organization, maintainable documentation, and predictable collaboration patterns across code, automation, and operational knowledge.

<!-- </llm> -->

<!-- <cmr cmd="repo.tags[name=repository.template]"> -->

`directive: <cmr cmd="repo.tags[name=repository.template]">`

<!-- </cmr> -->

## :clipboard: Requirements

<!-- <llm prompt="Requirements" applied> -->

Before working with this repository, ensure the following are available:

- Access to GitHub with permission to clone, fork, and open pull requests against the repository.
- Git installed locally and a standard command-line environment.
- The language runtime, toolchain, and package manager required by this project, as defined by the repository manifests and automation configuration.
- A local environment capable of running the repository's install, build, lint, and test commands.
- Any required environment variables, credentials, or service connections needed for development, CI, or deployment workflows.

Project-specific versions, setup commands, and external dependencies should be documented in the repository configuration and accompanying development guides.

<!-- </llm> -->

## :inbox_tray: Installation

<!-- <llm prompt="Installation" applied> -->

This repository is a template, so there is no installation step for the template itself.

To use it:

1. Click **Use this template** on GitHub to create a new repository from it.
2. Clone your new repository:
   ```bash
   git clone <your-repository-url>
   cd <your-repository-name>
   ```
3. Replace the template placeholders, example values, and repository-specific metadata with your project details.
4. Continue with the setup instructions for the actual software you build from this template.

If you are contributing to the template itself, clone this repository directly and work on the source files in place.

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Usage" applied> -->

Use this repository as a starting point for a new project repository.

1. Create a new repository from this template, or copy its contents into an existing repository.
2. Replace template variables and organization-specific placeholders, including `<!-- <var ...> -->` blocks, repository metadata, and documentation text.
3. Update the agent, prompt, skill, and knowledge files under `.github/` to match your project structure and workflow.
4. Review the generated documentation and diagrams, then remove any files or sections that do not apply to your repository.
5. Commit the customized result and continue normal repository development from there.

When adapting the template, keep the layer separation pattern intact: prompts route to agents, agents use skills, skills reference knowledge, and documentation reflects that structure.

<!-- </llm> -->

## :books: References

- [:page_facing_up: CODE\_OF\_CONDUCT.md](CODE_OF_CONDUCT.md)
- [:page_facing_up: CONTRIBUTING.md](CONTRIBUTING.md)
- [:page_facing_up: SECURITY.md](SECURITY.md)
- [:page_facing_up: ./docs/STRUCTURE.md](./docs/STRUCTURE.md) - Project Structure
- [:page_facing_up: ./docs/ORGANIZATION.md](./docs/ORGANIZATION.md) - Managing entity
