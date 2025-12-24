# 📋 Chimera Lab - Template Repository

<!--(version=1.0.0)-->

![Chimera-lab :lion: :goat: :snake:](https://github.com/chimera-lab/art/blob/main/logo/novem/chimera-lab-banner.png "Chimera-lab")

## 📖 Table of Content

- [Chimera Lab - Template Repository](#-chimera-lab---template-repository)
- [Introduction](#introduction)
- [Overview](#overview)
- [Usage](#usage)
- [Appendix](#appendix)

## 📣 Introduction

This is a base template repository for all Chimera Lab projects.

### Why This Template

This template provides a foundation for consistency across all Chimera Lab repositories, including:

- Standardized documentation structure
- Common GitHub configurations
- Contribution guidelines
- Metadata and organization standards

### How to Use This Template

1. Navigate to this template on GitHub
2. Click "Use this template"
3. Fill in your repository details
4. Clone and customize as needed

Alternatively, use the Chimera Lab CLI or GitHub CLI to create new repositories from this template.

## 🔭 Overview

### Requirements

To use this template, you need:

- `git` installed
- `gh` (GitHub CLI) or GitHub web access
- A GitHub account

### What's Included

- Standard README, CONTRIBUTING, LICENSE files
- GitHub issue templates
- Repository metadata (.chimera-lab/)
- Organization guidelines

## ⌨️ Usage

### Using GitHub CLI

```bash
gh repo create my-awesome-repository --public --template chimera-lab/repository.template
```

### Using GitHub Web Interface

1. Navigate to this template repository
2. Click "Use this template"
3. Create a new repository

### Using Chimera Lab CLI

```bash
cmr repo init my-repo --template repository.template --topic original.topic
```

## 📎 Appendix

### Notes

- To use a repository as a template, mark it as such in `Settings -> General -> Template repository`
- You can place `README.md` files outside the project root as documented in [GitHub - About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes#about-readmes)
- Template repositories are marked in `.chimera-lab/meta.json` with `is_template: true`

### References

- [GitHub Templates Documentation](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
- [Chimera Lab Organization](https://chimera-lab.org)
- [Chimera Lab CLI](https://github.com/chimera-lab/chimera-lab-cli.app)
