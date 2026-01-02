---
name: update-team
agent: prompt-engineer
description: Update architecture diagram with agents, prompts, and knowledge
---

# :file_folder: Update Team

## :book: Table of Contents

- [:file\_folder: Update Team](#file_folder-update-team)
  - [:world\_map: Resources Discovery](#world_map-resources-discovery)
    - [:compass: List Agents](#compass-list-agents)
    - [:compass: List Prompts](#compass-list-prompts)
    - [:compass: List Knowledge](#compass-list-knowledge)
  - [:world\_map: Read Content](#world_map-read-content)
    - [:compass: Process Agents](#compass-process-agents)
    - [:compass: Process Prompts](#compass-process-prompts)
    - [:compass: Process Knowledge](#compass-process-knowledge)
  - [:world\_map: Update Diagram](#world_map-update-diagram)
    - [:compass: Update PlantUML](#compass-update-plantuml)
    - [:compass: Validate](#compass-validate)

## :world_map: Resources Discovery

### :compass: List Agents

- Scan `.github/agents/`
- Extract names and descriptions
- Expected: 5-6 agents


### :compass: List Prompts

- Scan `.github/prompts/`
- Extract agent targets
- Expected: 10-11 prompts


### :compass: List Knowledge

- Scan `.github/knowledge/`
- Document purposes
- Expected: 4-5 files


## :world_map: Read Content

### :compass: Process Agents

- Read each agent file
- Extract name, description, role


### :compass: Process Prompts

- Read each prompt
- Identify target agent
- Note relationships


### :compass: Process Knowledge

- Read knowledge files
- Document purpose
- Map references


## :world_map: Update Diagram

### :compass: Update PlantUML

- Update `.github/copilot-team-components.plantuml`
- Add actual agents, prompts, knowledge
- Update relationships
- Maintain valid PlantUML syntax


### :compass: Validate

- All agents represented
- All prompts shown
- All knowledge files included
- Relationships correct
- Syntax valid
