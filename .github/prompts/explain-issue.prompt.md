---
name: explain-issue
agent: project-manager
description: Analyze GitHub issue and determine responsible agent
---

# :file_folder: Explain Issue

## :world_map: Analysis

### :compass: Retrieve Issue Details

- Get issue from GitHub
- Extract title, body, labels, milestone
- Identify context and references

### :compass: Analyze Requirements

- What needs to be done?
- Technical requirements identified?
- Dependencies documented?

### :compass: Determine Agent

- CLI work? → `cli-developer`
- Code architecture? → `python-architect`
- Documentation? → `technical-writer`
- Git/GitHub operations? → `repository-manager`
- Coordination/Planning? → `project-manager`

### :compass: Decompose

- Break into actionable steps
- Identify agents needed
- Order by dependencies

## :world_map: Output

- Issue summary
- Required agent(s)
- Task steps
- Estimated effort
