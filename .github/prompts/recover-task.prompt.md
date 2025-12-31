---
name: recover-task
agent: project-manager
description: Recover and restore todo list from previous context
---

# :file_folder: Recover Task

## :world_map: Recovery

### :compass: Analyze Context

- Review conversation history
- Find previous todo list states
- Identify last valid configuration

### :compass: Validate Structure

- Check id, title, description, status
- Ensure valid: not-started, in-progress, completed
- Identify incomplete or corrupted entries

### :compass: Restore

- Use `manage_todo_list` with operation="write"
- Include all recovered todos with original status
- Preserve progress and context

## :world_map: Report

### :compass: Confirm Recovery

- List todos by status
- Completed count
- In-progress count
- Not-started count
- Flag items needing attention

## :world_map: Recovery Sources

- Last `manage_todo_list` in conversation
- Explicit mentions in recent messages
- Inferred from completed work
