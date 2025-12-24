# 📋 Repository Template

<!--(version=1.0.0)-->

This is the base template for all Chimera Lab repositories.

## 📖 Table of content

- [About This Template](#about-this-template)
- [Using This Template](#using-this-template)
- [Repository Structure](#repository-structure)
- [Customizing for Your Repository](#customizing-for-your-repository)
- [Getting Help](#getting-help)
- [Related Resources](#related-resources)

## 🎯 About This Template

This template provides the foundation for creating new repositories within the Chimera Lab organization. It includes:

- Standard documentation structure (README, CONTRIBUTING, LICENSE)
- GitHub configuration (issue templates, workflows)
- Chimera Lab metadata (.chimera-lab/ directory)
- Contribution guidelines and community standards

## 🚀 Using This Template

### 1️⃣ GitHub Web Interface

1. Go to [repository.template on GitHub](https://github.com/chimera-lab/repository.template)
2. Click "Use this template"
3. Fill in your repository details
4. Clone and set up as described below

### 2️⃣ GitHub CLI

```bash
gh repo create chimera-lab/my-repo --template chimera-lab/repository.template --public
cd my-repo
git submodule add https://github.com/chimera-lab/repository.template.git .chimera-lab/.template
```

### 3️⃣ Chimera Lab CLI

```bash
cmr repo init my-repo.app --template repository.template --topic original.topic
```

## 📁 Repository Structure

```
my-repo/
├── .chimera-lab/              # Chimera Lab metadata
│   ├── meta.json              # Repository metadata
│   ├── settings.json          # Labels, milestones
│   ├── issues.json            # Issue templates
│   ├── milestones.json        # Milestone definitions
│   └── .template              # Submodule to template
├── .github/
│   ├── README.md              # Template documentation
│   └── ISSUE_TEMPLATE/        # GitHub issue templates
├── .gitignore                 # Standard ignore patterns
├── CONTRIBUTING.md            # Contribution guidelines
├── LICENSE                    # GPLv3 or custom license
└── README.md                  # Project README
```

## ✏️ Customizing for Your Repository

### 1️⃣ Update README.md

Replace this file with your project-specific README including:

- Project description and purpose
- Key features
- Installation instructions
- Usage examples
- Contributing guidelines
- License information

### 2️⃣ Update .chimera-lab/meta.json

Edit metadata to match your repository:

- Set `name` to your repository name
- Set `template` to your template type (e.g., "app.template", "project.template")
- Set `is_template` to `false` (unless this is a template)

### 3️⃣ Customize Contributing Guidelines

Edit CONTRIBUTING.md with:

- Project-specific contribution process
- Development setup for your language/framework
- Code style guidelines
- Testing requirements
- Pull request process

### 4️⃣ Choose a License

Replace LICENSE with appropriate license:

- GPLv3 (default for Chimera Lab)
- MIT (for packages)
- Apache 2.0 (for projects)

## 🆘 Getting Help

- **Issues**: Open an issue in your repository or in [chimera-lab/organization](https://github.com/chimera-lab/chimera-lab-organization)
- **Discussions**: Use GitHub discussions for questions
- **Documentation**: See [knowledge base](./.github/README.md)

## 📚 Related Resources

- [Chimera Lab Organization](https://chimera-lab.org)
- [Chimera Lab CLI](https://github.com/chimera-lab/chimera-lab-cli.app)
- [Organization Structure](https://github.com/chimera-lab/chimera-lab/tree/main/.github/docs)
- [Templates Overview](./.github/README.md)

---

**Template Version**: 1.0.0  
**Last Updated**: 2025-01-01

