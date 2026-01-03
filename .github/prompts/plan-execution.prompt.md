---
name: plan-execution
agent: project-manager
description: Create executable task lists from GitHub issues
---

# :file_folder: Plan Execution

## :book: Table of Contents

- [:file\_folder: Plan Execution](#file_folder-plan-execution)
  - [:book: Table of Contents](#book-table-of-contents)
  - [:world\_map: Issue Analysis](#world_map-issue-analysis)
    - [:compass: Fetch Issues](#compass-fetch-issues)
    - [:compass: Analyze Each](#compass-analyze-each)
    - [:compass: Validate Decomposition](#compass-validate-decomposition)
  - [:world\_map: Task Planning](#world_map-task-planning)
    - [:compass: Create Task List](#compass-create-task-list)
    - [:compass: Order Tasks](#compass-order-tasks)
    - [:compass: Assign Agents](#compass-assign-agents)
  - [:world\_map: Output](#world_map-output)

## :world_map: Issue Analysis

### :compass: Fetch Issues

- Single: `gh issue view <number>`
- Milestone: `gh issue list --milestone "v0.x.0"`
- Extract: title, body, labels, milestone

### :compass: Analyze Each

- Clear acceptance criteria?
- Technical requirements specified?
- Module/component identified?
- Dependencies documented?

### :compass: Validate Decomposition

- Single focused objective?
- Actionable steps clear?
- Estimated effort < 1 day?
- No ambiguous requirements?

## :world_map: Task Planning

### :compass: Create Task List

- Use `manage_todo_list` tool
- Format: `#<issue>: <action> - @<agent>`
- Include: issue, module, goal, steps, dependencies

### :compass: Order Tasks

- Foundation first: models, utilities
- Implementation: commands, modules
- Validation: tests, error handling
- Documentation: knowledge, docs
- Integration: workflows, releases

### :compass: Assign Agents

- `cli-developer` - Commands, Typer, Rich, CLI logic
- `python-architect` - Types, architecture, patterns
- `technical-writer` - Docs, knowledge, README
- `repository-manager` - Git, GitHub, releases
- `project-manager` - Coordination, planning

## :world_map: Output

- Complete task list with dependencies
- Agent assignments
- Execution order
- Success criteria
