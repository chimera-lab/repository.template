---
name: explain-issue
agent: project-manager
description: Analyze GitHub issue and determine responsible agent
---

# :file_folder: Explain Issue

## :book: Table of Contents

- [:file\_folder: Explain Issue](#file_folder-explain-issue)
  - [:book: Table of Contents](#book-table-of-contents)
  - [:world\_map: Analysis](#world_map-analysis)
    - [:compass: Retrieve Issue Details](#compass-retrieve-issue-details)
    - [:compass: Analyze Requirements](#compass-analyze-requirements)
    - [:compass: Determine Agent](#compass-determine-agent)
    - [:compass: Decompose](#compass-decompose)
  - [:world\_map: Output](#world_map-output)

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
