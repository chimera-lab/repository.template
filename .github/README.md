# :clipboard: Chimera Lab - Template Repository

## :book: Table of Contents

- [:book: Table of content](#table-of-content)
- [:mega: Introduction](#introduction)
  - [:memo: Why This Template](#why-this-template)
  - [:memo: How to Use This Template](#how-to-use-this-template)
- [:clipboard: :telescope: Overview](#overview)
  - [:memo: Requirements](#requirements)
  - [:memo: What's Included](#whats-included)
- [:rocket: :keyboard: Usage](#usage)
  - [:memo: Using GitHub CLI](#using-github-cli)
  - [:memo: Using GitHub Web Interface](#using-github-web-interface)
  - [:memo: Using Chimera Lab CLI](#using-chimera-lab-cli)
- [:paperclip: Appendix](#appendix)
  - [:memo: Notes](#notes)
  - [:memo: References](#references)

## :mega: Introduction

This is a base template repository for all Chimera Lab projects.

### :memo: Why This Template

This template provides a foundation for consistency across all Chimera Lab repositories, including:

- Standardized documentation structure
- Common GitHub configurations
- Contribution guidelines
- Metadata and organization standards


### :memo: How to Use This Template

1. Navigate to this template on GitHub
2. Click "Use this template"
3. Fill in your repository details
4. Clone and customize as needed


Alternatively, use the Chimera Lab CLI or GitHub CLI to create new repositories from this template.

## :clipboard: :telescope: Overview

### :memo: Requirements

To use this template, you need:

- `git` installed
- `gh` (GitHub CLI) or GitHub web access
- A GitHub account


### :memo: What's Included

- Standard README, CONTRIBUTING, LICENSE files
- GitHub issue templates
- Repository metadata (.chimera-lab/)
- Organization guidelines


## :rocket: :keyboard: Usage

### :memo: Using GitHub CLI

```bash
gh repo create my-awesome-repository --public --template chimera-lab/repository.template
```

### :memo: Using GitHub Web Interface

1. Navigate to this template repository
2. Click "Use this template"
3. Create a new repository


### :memo: Using Chimera Lab CLI

```bash
cmr repo init my-repo --template repository.template --topic original.topic
```

## :paperclip: Appendix

### :memo: Notes

- To use a repository as a template, mark it as such in `Settings -> General -> Template repository`
- You can place `README.md` files outside the project root as documented in [GitHub - About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes#about-readmes)
- Template repositories are marked in `.chimera-lab/meta.json` with `is_template: true`


### :memo: References

- [GitHub Templates Documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
- [Chimera Lab Organization](https://chimera-lab.org)
- [Chimera Lab CLI](https://github.com/chimera-lab/chimera-lab-cli.app)
