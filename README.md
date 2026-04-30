# :file_folder: <!-- <var key="repo.name" applied> -->repository.template<!-- </var> -->

<!-- <badges name="brand,license,last-commit,issues,stars" applied> -->

[![chimera-lab org](https://img.shields.io/badge/chimera--lab-org-6e40c9?style=flat-square)](https://github.com/chimera-lab)
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

This repository provides the standard foundation for a software project in the <!-- <var key="org.name" applied> -->chimera-lab.org<!-- </var> --> ecosystem. It combines repository structure, documentation conventions, agent-driven workflows, reusable skills, and supporting knowledge files so projects can start from a consistent, maintainable baseline.

The template is designed to make implementation, documentation, review, and maintenance predictable across repositories. It helps teams organize work clearly, keep automation and human contributors aligned, and extend the project without breaking established structure or organizational patterns.

<!-- </llm> -->

<!-- <cmr cmd="repo.tags[name=repository.template]"> -->

`directive: <cmr cmd="repo.tags[name=repository.template]">`

<!-- </cmr> -->

## :clipboard: Requirements

<!-- <llm prompt="Requirements" applied> -->

This repository is intended for projects hosted on **GitHub** and managed with **Git**. Documentation is expected to be maintained in **Markdown**, and repository automation should use standard **GitHub features** such as pull requests, issues, and GitHub Actions where applicable.

Projects using this template should also:

- follow the prescribed repository structure and organizational conventions;
- keep documentation, prompts, skills, and knowledge files aligned with their intended roles;
- update placeholder values and template content before production use;
- ensure contributors have access to the tools required by the project itself.

<!-- </llm> -->

## :inbox_tray: Installation

<!-- <llm prompt="Installation" applied> -->

Clone the repository, enter the project directory, and install dependencies with the package manager used by the project.

```bash
git clone <repository-url>
cd <repository-directory>
<package-manager> install
```

If the repository includes local environment configuration, create it before running the application:

```bash
cp .env.example .env
```

Use the versions and tooling defined in the repository configuration files and CI workflows to keep local setup consistent with the supported development environment.

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Usage" applied> -->

Use this repository as a starting point for a new project repository.

1. Create a new repository from this template.
2. Clone the generated repository locally.
3. Replace all placeholder values, example names, and organization-specific variables with your project details.
4. Update the documentation, agent definitions, prompts, skills, and knowledge files so they reflect the actual repository structure and workflow.
5. Remove any template-only content that does not apply to the new project, then commit the customized result.

This template is meant to be adapted, not consumed as a library or runtime dependency. Keep the generated repository aligned with the real project as it evolves.

<!-- </llm> -->

## :books: References

- [:page_facing_up: CODE\_OF\_CONDUCT.md](CODE_OF_CONDUCT.md)
- [:page_facing_up: CONTRIBUTING.md](CONTRIBUTING.md)
- [:page_facing_up: SECURITY.md](SECURITY.md)
- [:page_facing_up: ./docs/STRUCTURE.md](./docs/STRUCTURE.md) - Project Structure
- [:page_facing_up: ./docs/ORGANIZATION.md](./docs/ORGANIZATION.md) - Managing entity
