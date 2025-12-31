---
name: fix-context
agent: prompt-engineer
description: Validate and improve agents, prompts, and knowledge files
---

# :file_folder: Fix Context

## :world_map: Information Gathering

### :compass: Discover Files

- List: `.github/agents/` - all `.agent.md` files
- List: `.github/prompts/` - all `.prompt.md` files
- List: `.github/knowledge/` - all `.md` files
- Document purposes and relationships

## :world_map: Validation

### :compass: Check Names

- Agents: `lowercase-with-hyphens.agent.md`
- Prompts: `lowercase-with-hyphens.prompt.md`
- Knowledge: `lowercase-with-hyphens.knowledge.md`

### :compass: Check Content

- Agents: Have role, goal, limitations, instructions
- Prompts: Have agent field, description, clear purpose
- Knowledge: Self-contained, no file references

### :compass: Check References

- Agents: Reference only knowledge files
- Prompts: Reference only knowledge files
- No agent-to-agent or prompt-to-prompt references

## :world_map: Improvements

### :compass: Provide Feedback

- List issues found
- Suggest fixes
- Maintain separation of concerns
