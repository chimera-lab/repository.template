______________________________________________________________________

## :warning: agent: project-manager description: Read GitHub issues, validate decomposition quality, and create executable task lists with agent assignments

# Plan Execution

## :book: Table of Contents

- [Plan Execution](#plan-execution)
  - [:book: Table of Contents](#book-table-of-contents)
  - [:warning: agent: project-manager description: Read GitHub issues, validate decomposition quality, and create executable task lists with agent assignments](#warning-agent-project-manager-description-read-github-issues-validate-decomposition-quality-and-create-executable-task-lists-with-agent-assignments)
  - [:book: Table of content](#book-table-of-content)
  - [:book: Table of content](#book-table-of-content)
  - [Required Information](#required-information)
  - [Execution Steps](#execution-steps)
    - [:warning: 1. Read and Analyze Issues](#warning-1-read-and-analyze-issues)
    - [2. Validate Decomposition Quality](#2-validate-decomposition-quality)
    - [3. Create Task List](#3-create-task-list)
    - [:package: 4. Task Ordering and Dependencies](#package-4-task-ordering-and-dependencies)
    - [5. Execute Task Creation](#5-execute-task-creation)
  - [Output Format](#output-format)
  - [Validation Checklist](#validation-checklist)
  - [Best Practices](#best-practices)
  - [Common Patterns](#common-patterns)

## :book: Table of content

- [Table of content](#table-of-content)
  - [agent: project-manager
    description: Read GitHub issues, validate decomposition quality, and create executable task lists with agent assignments](#agent-project-manager-description-read-github-issues-validate-decomposition-quality-and-create-executable-task-lists-with-agent-assignments)
- [Plan Execution](#plan-execution)
  - [:book: Table of content](#book-table-of-content)
  - [Required Information](#required-information)
  - [Execution Steps](#execution-steps)
    - [:warning: 1. Read and Analyze Issues](#warning-1-read-and-analyze-issues)
    - [2. Validate Decomposition Quality](#2-validate-decomposition-quality)
    - [3. Create Task List](#3-create-task-list)
    - [:package: 4. Task Ordering and Dependencies](#package-4-task-ordering-and-dependencies)
    - [5. Execute Task Creation](#5-execute-task-creation)
  - [Output Format](#output-format)
  - [Validation Checklist](#validation-checklist)
  - [Best Practices](#best-practices)
  - [Common Patterns](#common-patterns)

## :book: Table of content

- [agent: project-manager
  description: Read GitHub issues, validate decomposition quality, and create executable task lists with agent assignments](#agent-project-manager-description-read-github-issues-validate-decomposition-quality-and-create-executable-task-lists-with-agent-assignments)
- [Table of content](#table-of-content)
- [Required Information](#required-information)
- [Execution Steps](#execution-steps)
  - [1. Read and Analyze Issues](#1-read-and-analyze-issues)
  - [2. Validate Decomposition Quality](#2-validate-decomposition-quality)
  - [3. Create Task List](#3-create-task-list)
  - [4. Task Ordering and Dependencies](#4-task-ordering-and-dependencies)
  - [5. Execute Task Creation](#5-execute-task-creation)
- [Output Format](#output-format)
- [Validation Checklist](#validation-checklist)
- [Best Practices](#best-practices)
- [Common Patterns](#common-patterns)

## Required Information

- **Issue number(s)**: Single issue or milestone issues to process
- **Priority order**: Optional prioritization guidance
- **Constraints**: Dependencies, blockers, or sequencing requirements

## Execution Steps

### :warning: 1. Read and Analyze Issues

Fetch issue details using GitHub CLI:

```bash

## Single issue

gh issue view <number> --json number,title,body,labels,milestone,assignees

## :warning: All issues in milestone

gh issue list --milestone "v0.x.0" --json number,title,body,labels,state
```

**Analyze Each Issue**:

- ✅ Clear acceptance criteria defined
- ✅ Technical requirements specified
- ✅ Module/component identified
- ✅ Dependencies documented
- ⚠️ Complexity estimated (S/M/L/XL)

### 2. Validate Decomposition Quality

**Check if issue is properly decomposed**:

**Well-Decomposed Issue** (ready for execution):

- Single, focused objective
- Actionable steps clear
- Estimated effort < 1 day
- No ambiguous requirements
- Module/component specified
- Testing approach defined

**Needs Further Decomposition** (create sub-tasks):

- Multiple objectives in one issue
- Complexity > 1 day (Large or XL)
- Cross-cutting concerns (affects multiple modules)
- Unclear implementation path
- Missing technical details

**Action**:

- If decomposition needed: Comment on issue with breakdown suggestions and stop
- If well-decomposed: Proceed to task creation

### 3. Create Task List

**Use `manage_todo_list` tool** to create structured execution plan:

**Task Title Format**: `#<issue-number>: <action> - @<agent>`

**Examples**:

- `#42: Implement graph templates command - @cli-developer`
- `#43: Add RepositoryGraph type model - @python-architect`
- `#44: Update graph documentation - @technical-writer`
- `#45: Create graph integration tests - @cli-developer`

**Task Description Format**:

```markdown
**Issue**: #<number> - <issue-title>
**Module**: <affected-module>
**Goal**: <what-needs-to-be-done>

**Implementation Details**:

- Step 1: Specific action with file/function references
- Step 2: Another specific action
- Step 3: Testing/validation step

**Dependencies**: <other-task-ids-if-any>
**Files**: <key-files-to-modify>
```

**Agent Assignment Guide**:

- `@cli-developer`: Commands, Typer integration, Rich formatting, CLI logic
- `@python-architect`: Type models, architecture, patterns, module design
- `@technical-writer`: Documentation, knowledge base, README updates
- `@repository-manager`: Git operations, GitHub workflows, releases, CI/CD
- `@project-manager`: Coordination, planning, milestone tracking

### :package: 4. Task Ordering and Dependencies

**Sequence tasks by**:

1. **Foundation first**: Type models, core utilities, base patterns
1. **Implementation**: Commands, modules, integrations
1. **Validation**: Tests, error handling, edge cases
1. **Documentation**: Knowledge base, docs, README updates
1. **Integration**: GitHub workflows, releases, deployment

**Mark dependencies**:

```json
{
  "id": 3,
  "title": "#42: Implement graph templates command - @cli-developer",
  "description": "...\n**Dependencies**: Task #1 (RepositoryGraph model), Task #2 (GraphML utilities)",
  "status": "not-started"
}
```

### 5. Execute Task Creation

**Use `manage_todo_list` with operation="write"**:

```json
{
  "operation": "write",
  "todoList": [
    {
      "id": 1,
      "title": "#43: Add RepositoryGraph type model - @python-architect",
      "description": "**Issue**: #43 - Create RepositoryGraph Pydantic model\n**Module**: src/cmrlab/types/repository.py\n**Goal**: Define type-safe graph representation for GraphML export\n\n**Implementation Details**:\n- Add RepositoryGraph model with nodes and edges fields\n- Define NodeModel (id, label, type, metadata)\n- Define EdgeModel (source, target, relationship)\n- Add validation for graph structure integrity\n\n**Dependencies**: None\n**Files**: src/cmrlab/types/repository.py",
      "status": "not-started"
    },
    {
      "id": 2,
      "title": "#42: Implement graph templates command - @cli-developer",
      "description": "**Issue**: #42 - Add cmr graph templates CLI command\n**Module**: src/cmrlab/graph.py, src/cmrlab/app.py\n**Goal**: Create command to list and apply GraphML templates\n\n**Implementation Details**:\n- Add `graph_templates()` function to graph.py\n- Integrate with Typer app in app.py under graph command group\n- Use Walker to discover template files in .chimera-lab/templates/\n- Format output with Rich table showing template names and descriptions\n- Add --apply flag to apply selected template\n\n**Dependencies**: Task #1 (RepositoryGraph model)\n**Files**: src/cmrlab/graph.py, src/cmrlab/app.py",
      "status": "not-started"
    },
    {
      "id": 3,
      "title": "#44: Update graph documentation - @technical-writer",
      "description": "**Issue**: #44 - Document graph templates feature\n**Module**: .github/knowledge/commands.knowledge.md\n**Goal**: Add documentation for new graph templates command\n\n**Implementation Details**:\n- Update commands.knowledge.md with graph templates syntax\n- Add examples of template usage to docs/CLI_GUIDELINES.md\n- Create .chimera-lab/templates/example.graphml reference\n- Document template file format requirements\n\n**Dependencies**: Task #2 (command implementation)\n**Files**: .github/knowledge/commands.knowledge.md, .github/docs/CLI_GUIDELINES.md",
      "status": "not-started"
    }
  ]
}
```

## Output Format

**Confirmation Message**:

```markdown
✅ Task list created: <N> tasks from <M> issues

**Execution Order**:

1. Task #1: #43 - Add RepositoryGraph type model (@python-architect)
2. Task #2: #42 - Implement graph templates command (@cli-developer)  
3. Task #3: #44 - Update graph documentation (@technical-writer)

**Agent Distribution**:

- @python-architect: 1 task
- @cli-developer: 1 task
- @technical-writer: 1 task

**Ready to Start**: Use `@<agent> work` prompt to execute tasks
```

## Validation Checklist

Before creating task list:

- [ ] All issues read and analyzed
- [ ] Decomposition quality validated
- [ ] Tasks have clear titles with issue ID and agent
- [ ] Descriptions include implementation details
- [ ] Dependencies identified and documented
- [ ] Logical execution sequence established
- [ ] Agent assignments appropriate for task type
- [ ] Each task is actionable and well-scoped

## Best Practices

**Task Granularity**:

- ✅ 1 task = 1-4 hours of focused work
- ✅ Clear start and end state
- ❌ Avoid multi-day monolithic tasks
- ❌ Don't split atomic operations

**Agent Selection**:

- Match task type to agent expertise
- Consider workload distribution
- Respect module ownership patterns
- Enable parallel execution when possible

**Description Quality**:

- Specific file and function references
- Clear acceptance criteria
- Testing requirements included
- Context links to knowledge base

**Dependency Management**:

- Explicit dependency IDs in descriptions
- Logical execution sequence
- Avoid circular dependencies
- Enable parallel tracks when possible

## Common Patterns

**Feature Implementation Sequence**:

1. Type models (@python-architect)
1. Core logic/utilities (@cli-developer)
1. CLI command integration (@cli-developer)
1. Tests and validation (@cli-developer)
1. Documentation updates (@technical-writer)

**Bug Fix Sequence**:

1. Root cause analysis (@relevant-agent)
1. Fix implementation (@relevant-agent)
1. Regression test (@cli-developer)
1. Documentation update if needed (@technical-writer)

**Refactor Sequence**:

1. Design new structure (@python-architect)
1. Implement changes (@cli-developer)
1. Migration of existing code (@cli-developer)
1. Update documentation (@technical-writer)
1. Cleanup and verification (@repository-manager)

______________________________________________________________________

**After task list creation**: Use individual agent prompts (`work.prompt.md`) to execute tasks sequentially or assign to team members.
