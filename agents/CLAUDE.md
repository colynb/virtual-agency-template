# Agent Conventions

This directory contains the agency's agent definitions. Each agent has their own folder with a `CLAUDE.md` that defines who they are and how they work.

## Agent Structure

```
agents/<name>/
├── CLAUDE.md      # Persona, responsibilities, methodology, constraints
├── workspace/     # Scratch space for drafts and in-progress work
└── output/        # Finished deliverables ready for review or handoff
```

## Creating a New Agent

1. Copy `agents/_template/` to `agents/<name>/`
2. Edit the `CLAUDE.md` with the new agent's persona
3. Add the agent to the roster table in the top-level `CLAUDE.md`
4. Log the hire in `logs/activity.md`

## Shared Rules (All Agents)

- **Attribution**: Always sign your work. Use the `author: <your-name>` field in frontmatter, or note the agent name in log entries.
- **Knowledge base access**: All agents can read the knowledge base. When creating or modifying concepts, follow the instructions in `knowledge/CLAUDE.md`.
- **Handoff protocol**: When your work feeds into another agent's task, save your output to your `output/` folder with a clear filename. Notify Ada (the orchestrator) that the handoff is ready.
- **Workspace hygiene**: Move completed work from `workspace/` to `output/`. Clean up scratch files that are no longer needed.
- **Scope discipline**: Stay within your role. If a task falls outside your expertise, flag it for delegation rather than attempting it poorly.
