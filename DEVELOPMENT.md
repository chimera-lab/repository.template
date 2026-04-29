# :file_folder: Development Environment Setup

## :book: Table of Contents

- [:file_folder: Development Environment Setup](./#file_folder-development-environment-setup)
  - [:clipboard: Requirements](./#clipboard-requirements)
  - [:inbox_tray: Installation](./#inbox_tray-installation)
    - [:inbox_tray: Clone the repository](./#inbox_tray-clone-the-repository)
    - [:inbox_tray: Create development environment](./#inbox_tray-create-development-environment)
    - [:inbox_tray: Install dependencies](./#inbox_tray-install-dependencies)
    - [:inbox_tray: Install pre-commit hooks (optional but recommended)](./#inbox_tray-install-pre-commit-hooks-optional-but-recommended)
  - [:keyboard: Usage](./#keyboard-usage)
  - [:toolbox: Tools](./#toolbox-tools)
    - [:toolbox: Running Tests](./#toolbox-running-tests)
    - [:toolbox: Code Quality](./#toolbox-code-quality)
    - [:toolbox: CMR Pipeline](./#toolbox-cmr-pipeline)
    - [:toolbox: Pre-commit Hooks](./#toolbox-pre-commit-hooks)
  - [:wrench: Configuration](./#wrench-configuration)
  - [:control_knobs: Customization](./#control_knobs-customization)
  - [:hammer_and_wrench: Common Problems](./#hammer_and_wrench-common-problems)
    - [:hammer_and_wrench: Dependency errors](./#hammer_and_wrench-dependency-errors)
    - [:hammer_and_wrench: Pre-commit failures](./#hammer_and_wrench-pre-commit-failures)
    - [:hammer_and_wrench: Test failures](./#hammer_and_wrench-test-failures)

## :clipboard: Requirements

<!-- <llm prompt="Development.Requirements" applied> -->

- Git installed
- Your project's runtime environment (Node.js, Python, Go, etc.)
- VS Code (recommended) or your preferred editor

<!-- </llm> -->

## :inbox_tray: Installation

### :inbox_tray: Clone the repository

```bash
git clone <!-- <var key="repo.remote" applied> -->git@github.com:chimera-lab/repository.template.git<!-- </var> -->
cd <!-- <var key="repo.name" applied> -->repository.template<!-- </var> -->
```

### :inbox_tray: Create development environment

<!-- <llm prompt="Development.Installation" applied> -->

Describe how to bootstrap an isolated development environment for this repository (virtualenv, nvm, Docker, etc.) including any prerequisite tools.

<!-- </llm> -->

### :inbox_tray: Install dependencies

<!-- <llm prompt="Development.InstallDependencies" applied> -->

```bash
# Use the appropriate command for your project type
make install
```

<!-- </llm> -->

### :inbox_tray: Install pre-commit hooks (optional but recommended)

<!-- <llm prompt="Development.PreCommitHooks" applied> -->

```bash
pre-commit install
```

<!-- </llm> -->

## :keyboard: Usage

<!-- <llm prompt="Development.Usage" applied> -->

Use Make (recommended) for common development tasks:

```bash
# Install dependencies
make install

# Run tests
make test

# Run linting
make lint

# Format code
make format

# Run all checks
make check

# Clean build artifacts
make clean

# Set up development environment
make setup

# Run the full CMR pipeline
make cmr-pipeline
```

<!-- </llm> -->

## :toolbox: Tools

### :toolbox: Running Tests

<!-- <llm prompt="Development.Tests" applied> -->

Explain how to run the test suite, the conventions tests must follow, and how to scope tests to a specific module or feature.

<!-- </llm> -->

### :toolbox: Code Quality

<!-- <llm prompt="Development.CodeQuality" applied> -->

Document the code quality tooling: linters, formatters, type checkers, and how to invoke each one (manually and via `make`).

<!-- </llm> -->

### :toolbox: CMR Pipeline

<!-- <llm prompt="Development.CmrPipeline" applied> -->

Use the CMR pipeline to keep template consumers synchronized and documentation validated.

```bash
# 1) Validate docs and directives
make cmr-check

# 2) Inspect template differences
make cmr-template-diff

# 3) Apply template changes
make cmr-template-update

# 4) Refresh directive output and TOC
make cmr-render

# 5) Run full flow in one command
make cmr-pipeline
```

Pipeline order:

```text
check -> template diff -> template update -> render -> check
```

Notes:

- `cmr-check` validates docs and tag directives.
- `cmr-template-diff` is safe to run repeatedly before update.
- `cmr-render` uses `cmr docs fix --tags` and `cmr docs fix -r toc` for deterministic refresh.

<!-- </llm> -->

### :toolbox: Pre-commit Hooks

<!-- <llm prompt="Development.PreCommitTools" applied> -->

Pre-commit hooks automatically run checks before commits:

```bash
# Install hooks
pre-commit install

# Run manually
pre-commit run --all-files
```

<!-- </llm> -->

## :wrench: Configuration

<!-- <llm prompt="Development.Configuration" applied> -->

If using VS Code, the workspace is pre-configured with:

- **Recommended extensions** (will prompt to install)
- **Editor settings** (formatting, linting)
- **Debug configurations** for your project type
- **Task definitions** for common operations

<!-- </llm> -->

## :control_knobs: Customization

<!-- <llm prompt="Development.Customization" applied> -->

List the customization points exposed by the repository: configuration files, environment variables, feature flags, and template variables that downstream consumers can override.

<!-- </llm> -->

## :hammer_and_wrench: Common Problems

<!-- <llm prompt="Development.CommonProblems" applied> -->

### :hammer_and_wrench: Dependency errors

Ensure you've installed all required dependencies

### :hammer_and_wrench: Pre-commit failures

Run `pre-commit run --all-files` to fix

### :hammer_and_wrench: Test failures

Check that all dependencies are correctly installed

<!-- </llm> -->
